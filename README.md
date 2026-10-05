# tsht99

Webエンジニア。

TypeScript を中心に、Web アプリケーションの設計・実装・テスト・運用まで取り組んでいます。  
特に、業務ルールをコード上の境界として整理すること、変更に耐えられる設計、自動テストや開発ルールによる品質保証に関心があります。

## 技術スタック

- **Language:** TypeScript
- **Frontend:** React / Next.js, Vue.js
- **Backend:** Next.js Server Actions, NestJS
- **Database:** PostgreSQL, Drizzle ORM
- **Testing:** Vitest, Playwright, Testcontainers
- **Other:** Vercel, GitHub Actions, Sentry

## 主な成果物

### [TimeCard](https://github.com/tsht99/time-card-portfolio)

小規模店舗向けの勤怠管理 Web アプリケーションです。  
実運用している非公開リポジトリから、安全に公開できる時点を切り出したポートフォリオ用の公開スナップショットです。

スタッフの打刻だけでなく、管理者による勤怠訂正・取消、変更履歴、時給履歴、給与見込みまで扱います。

#### 特に見ていただきたいポイント

- **Modular Monolith**
  - Users / Access、Attendance、Payroll / Hourly Wage を業務境界として分離
  - Domain / Application を Next.js や ORM などの具体技術から分離
- **Attendance Event Stream**
  - 出勤・退勤・訂正・取消をイベントとして保持
  - Current State Projection を通常の読み取りに利用
- **整合性・競合制御**
  - Domain、Application、Database の複数境界で業務ルールを保証
  - transaction / constraint / version による競合検知
- **Testing**
  - Small / Medium Test を使い分け
  - PostgreSQL・Next.js runtime・Playwright を含む統合的な検証
- **AI-assisted Development**
  - AI エージェントを開発補助に利用
  - repository-local rule と機械的 guard により変更範囲や migration 操作を制御

より詳しい設計意図と実装へのリンクは、  
👉 **[TimeCard README](https://github.com/tsht99/time-card-portfolio#readme)**

から確認できます。

## 開発で大切にしていること

機能を実装して終わりではなく、要件・設計・テスト・デプロイ・運用まで含めて、  
「なぜこの設計にしたのか」を説明できるソフトウェア開発を大切にしています。

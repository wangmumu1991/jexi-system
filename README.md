[捷希科技内部系捷希科技内部系统.html](https://github.com/user-attachments/files/26922188/default.html)
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>深圳市捷希科技有限公司-内部系统</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #1e5aa8;
            --primary-dark: #154785;
            --primary-light: #2d7cd6;
            --secondary-color: #4a90d9;
            --accent-color: #f39c12;
            --success-color: #27ae60;
            --danger-color: #e74c3c;
            --text-dark: #2c3e50;
            --text-light: #7f8c8d;
            --bg-light: #f5f7fa;
            --bg-white: #ffffff;
            --border-color: #e1e8ed;
            --shadow: 0 2px 12px rgba(30, 90, 168, 0.15);
            --shadow-hover: 0 4px 20px rgba(30, 90, 168, 0.25);
        }

        body {
            font-family: 'Microsoft YaHei', 'PingFang SC', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #1e5aa8 0%, #2980b9 50%, #3498db 100%);
            min-height: 100vh;
            color: var(--text-dark);
        }

        /* 登录页面样式 */
        .login-container {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .login-box {
            background: var(--bg-white);
            border-radius: 16px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            width: 100%;
            max-width: 420px;
            overflow: hidden;
        }

        .login-header {
            background: linear-gradient(135deg, var(--primary-color), var(--primary-light));
            color: white;
            padding: 40px 30px;
            text-align: center;
        }

        .login-header h1 {
            font-size: 24px;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .login-header p {
            font-size: 14px;
            opacity: 0.9;
        }

        .login-header .logo {
            width: 70px;
            height: 70px;
            background: rgba(255,255,255,0.2);
            border-radius: 50%;
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 32px;
        }

        .login-form {
            padding: 40px 30px;
        }

        .form-group {
            margin-bottom: 24px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--text-dark);
        }

        .form-group input {
            width: 100%;
            padding: 14px 16px;
            border: 2px solid var(--border-color);
            border-radius: 8px;
            font-size: 15px;
            transition: all 0.3s ease;
        }

        .form-group input:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(30, 90, 168, 0.1);
        }

        .login-btn {
            width: 100%;
            padding: 16px;
            background: linear-gradient(135deg, var(--primary-color), var(--primary-light));
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .login-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(30, 90, 168, 0.4);
        }

        .login-footer {
            text-align: center;
            padding: 20px 30px;
            background: var(--bg-light);
            font-size: 13px;
            color: var(--text-light);
        }

        .demo-accounts {
            margin-top: 20px;
            padding: 15px;
            background: #f8f9fa;
            border-radius: 8px;
            font-size: 13px;
        }

        .demo-accounts h4 {
            margin-bottom: 10px;
            color: var(--text-dark);
        }

        .demo-accounts p {
            margin: 5px 0;
            color: var(--text-light);
        }

        .demo-accounts code {
            background: #e9ecef;
            padding: 2px 6px;
            border-radius: 4px;
            color: var(--primary-color);
        }

        .error-msg {
            color: var(--danger-color);
            font-size: 13px;
            margin-top: 8px;
            display: none;
        }

        /* 主系统样式 */
        .main-system {
            display: none;
            min-height: 100vh;
        }

        /* 顶部导航 */
        .top-nav {
            background: linear-gradient(135deg, var(--primary-color), var(--primary-dark));
            color: white;
            padding: 0 30px;
            height: 70px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .nav-brand {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .nav-brand .logo-icon {
            width: 45px;
            height: 45px;
            background: rgba(255,255,255,0.2);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
        }

        .nav-brand h1 {
            font-size: 18px;
            font-weight: 600;
        }

        .nav-user {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .user-info {
            display: flex;
            align-items: center;
            gap: 10px;
            cursor: pointer;
            padding: 8px 15px;
            border-radius: 8px;
            transition: background 0.3s;
        }

        .user-info:hover {
            background: rgba(255,255,255,0.1);
        }

        .user-avatar {
            width: 40px;
            height: 40px;
            background: var(--accent-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 600;
        }

        .user-name {
            font-weight: 500;
        }

        .user-role {
            font-size: 12px;
            opacity: 0.8;
        }

        .logout-btn {
            padding: 10px 20px;
            background: rgba(255,255,255,0.15);
            border: 1px solid rgba(255,255,255,0.3);
            color: white;
            border-radius: 6px;
            cursor: pointer;
            font-size: 14px;
            transition: all 0.3s;
        }

        .logout-btn:hover {
            background: rgba(255,255,255,0.25);
        }

        /* 侧边栏 */
        .main-layout {
            display: flex;
            min-height: calc(100vh - 70px);
        }

        .sidebar {
            width: 260px;
            background: var(--bg-white);
            border-right: 1px solid var(--border-color);
            padding: 20px 0;
            overflow-y: auto;
        }

        .sidebar-menu {
            list-style: none;
        }

        .menu-item {
            padding: 14px 25px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 12px;
            transition: all 0.3s;
            border-left: 4px solid transparent;
            font-size: 15px;
        }

        .menu-item:hover {
            background: var(--bg-light);
            color: var(--primary-color);
        }

        .menu-item.active {
            background: linear-gradient(90deg, rgba(30, 90, 168, 0.1), transparent);
            border-left-color: var(--primary-color);
            color: var(--primary-color);
            font-weight: 500;
        }

        .menu-item .icon {
            width: 36px;
            height: 36px;
            background: var(--bg-light);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            transition: all 0.3s;
        }

        .menu-item.active .icon,
        .menu-item:hover .icon {
            background: var(--primary-color);
            color: white;
        }

        .menu-divider {
            height: 1px;
            background: var(--border-color);
            margin: 15px 0;
        }

        .admin-only {
            display: none;
        }

        body.is-admin .admin-only {
            display: flex;
        }

        /* 主内容区 */
        .main-content {
            flex: 1;
            padding: 30px;
            background: var(--bg-light);
            overflow-y: auto;
        }

        .page-header {
            margin-bottom: 30px;
        }

        .page-header h2 {
            font-size: 26px;
            color: var(--text-dark);
            margin-bottom: 8px;
        }

        .page-header p {
            color: var(--text-light);
        }

        /* 公告模块 */
        .announcement-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 16px;
            padding: 25px;
            color: white;
            margin-bottom: 30px;
        }

        .announcement-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }

        .announcement-header h3 {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 18px;
        }

        .announcement-list {
            display: grid;
            gap: 12px;
        }

        .announcement-item {
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(10px);
            border-radius: 10px;
            padding: 16px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            cursor: pointer;
            transition: all 0.3s;
        }

        .announcement-item:hover {
            background: rgba(255,255,255,0.25);
            transform: translateX(5px);
        }

        .announcement-content {
            flex: 1;
        }

        .announcement-title {
            font-weight: 500;
            margin-bottom: 4px;
        }

        .announcement-time {
            font-size: 12px;
            opacity: 0.8;
        }

        .announcement-tag {
            padding: 4px 12px;
            background: rgba(255,255,255,0.2);
            border-radius: 20px;
            font-size: 12px;
        }

        /* 内容卡片 */
        .content-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 24px;
            margin-bottom: 30px;
        }

        .content-card {
            background: var(--bg-white);
            border-radius: 12px;
            padding: 25px;
            box-shadow: var(--shadow);
            transition: all 0.3s;
        }

        .content-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-hover);
        }

        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 20px;
        }

        .card-icon {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
        }

        .card-icon.training { background: linear-gradient(135deg, #4facfe, #00f2fe); }
        .card-icon.business { background: linear-gradient(135deg, #43e97b, #38f9d7); }
        .card-icon.announcement { background: linear-gradient(135deg, #fa709a, #fee140); }
        .card-icon.admin { background: linear-gradient(135deg, #a18cd1, #fbc2eb); }

        .card-title {
            font-size: 18px;
            color: var(--text-dark);
            margin-bottom: 8px;
        }

        .card-desc {
            font-size: 14px;
            color: var(--text-light);
            line-height: 1.6;
        }

        .card-count {
            background: var(--bg-light);
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 13px;
            color: var(--primary-color);
            font-weight: 500;
        }

        /* 子模块列表 */
        .module-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .module-item {
            background: var(--bg-white);
            border-radius: 12px;
            padding: 25px;
            cursor: pointer;
            box-shadow: var(--shadow);
            transition: all 0.3s;
            border: 2px solid transparent;
        }

        .module-item:hover {
            transform: translateY(-3px);
            box-shadow: var(--shadow-hover);
            border-color: var(--primary-color);
        }

        .module-icon {
            width: 60px;
            height: 60px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            margin-bottom: 15px;
        }

        .module-icon.onboarding { background: linear-gradient(135deg, #667eea, #764ba2); }
        .module-icon.job { background: linear-gradient(135deg, #f093fb, #f5576c); }
        .module-icon.skill { background: linear-gradient(135deg, #4facfe, #00f2fe); }
        .module-icon.project { background: linear-gradient(135deg, #43e97b, #38f9d7); }
        .module-icon.product { background: linear-gradient(135deg, #fa709a, #fee140); }
        .module-icon.business-doc { background: linear-gradient(135deg, #a18cd1, #fbc2eb); }
        .module-icon.design { background: linear-gradient(135deg, #ff9a9e, #fecfef); }

        .module-title {
            font-size: 17px;
            font-weight: 600;
            color: var(--text-dark);
            margin-bottom: 8px;
        }

        .module-count {
            font-size: 13px;
            color: var(--text-light);
        }

        /* 详情页面 */
        .detail-page {
            display: none;
        }

        .detail-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
        }

        .back-btn {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 10px 20px;
            background: var(--bg-white);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            cursor: pointer;
            font-size: 14px;
            color: var(--text-dark);
            transition: all 0.3s;
        }

        .back-btn:hover {
            border-color: var(--primary-color);
            color: var(--primary-color);
        }

        .add-btn {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 12px 24px;
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 14px;
            font-weight: 500;
            transition: all 0.3s;
        }

        .add-btn:hover {
            background: var(--primary-dark);
        }

        .add-btn.hidden {
            display: none;
        }

        /* 文档列表 */
        .doc-list {
            display: grid;
            gap: 16px;
        }

        .doc-item {
            background: var(--bg-white);
            border-radius: 12px;
            padding: 20px 25px;
            box-shadow: var(--shadow);
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.3s;
        }

        .doc-item:hover {
            transform: translateX(5px);
            box-shadow: var(--shadow-hover);
        }

        .doc-info {
            display: flex;
            align-items: center;
            gap: 16px;
            flex: 1;
        }

        .doc-icon {
            width: 48px;
            height: 48px;
            background: linear-gradient(135deg, var(--primary-color), var(--primary-light));
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 20px;
        }

        .doc-details h4 {
            font-size: 16px;
            color: var(--text-dark);
            margin-bottom: 5px;
        }

        .doc-meta {
            font-size: 13px;
            color: var(--text-light);
            display: flex;
            gap: 15px;
        }

        .doc-actions {
            display: flex;
            gap: 10px;
        }

        .doc-actions button {
            padding: 8px 14px;
            border: 1px solid var(--border-color);
            border-radius: 6px;
            background: white;
            cursor: pointer;
            font-size: 13px;
            transition: all 0.3s;
        }

        .doc-actions .view-btn:hover {
            border-color: var(--primary-color);
            color: var(--primary-color);
        }

        .doc-actions .edit-btn:hover {
            border-color: var(--accent-color);
            color: var(--accent-color);
        }

        .doc-actions .delete-btn:hover {
            border-color: var(--danger-color);
            color: var(--danger-color);
        }

        .doc-actions.hidden {
            display: none;
        }

        /* 弹窗样式 */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0,0,0,0.5);
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 2000;
            padding: 20px;
        }

        .modal-overlay.active {
            display: flex;
        }

        .modal {
            background: var(--bg-white);
            border-radius: 16px;
            width: 100%;
            max-width: 500px;
            max-height: 90vh;
            overflow-y: auto;
            animation: modalIn 0.3s ease;
        }

        @keyframes modalIn {
            from {
                opacity: 0;
                transform: scale(0.9) translateY(-20px);
            }
            to {
                opacity: 1;
                transform: scale(1) translateY(0);
            }
        }

        .modal-header {
            padding: 24px 30px;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .modal-header h3 {
            font-size: 20px;
            color: var(--text-dark);
        }

        .modal-close {
            width: 36px;
            height: 36px;
            border: none;
            background: var(--bg-light);
            border-radius: 50%;
            cursor: pointer;
            font-size: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
        }

        .modal-close:hover {
            background: var(--danger-color);
            color: white;
        }

        .modal-body {
            padding: 30px;
        }

        .modal-body .form-group {
            margin-bottom: 20px;
        }

        .modal-body textarea {
            width: 100%;
            padding: 14px 16px;
            border: 2px solid var(--border-color);
            border-radius: 8px;
            font-size: 15px;
            font-family: inherit;
            resize: vertical;
            min-height: 120px;
        }

        .modal-body textarea:focus,
        .modal-body select:focus {
            outline: none;
            border-color: var(--primary-color);
        }

        .modal-body select {
            width: 100%;
            padding: 14px 16px;
            border: 2px solid var(--border-color);
            border-radius: 8px;
            font-size: 15px;
            background: white;
        }

        .modal-footer {
            padding: 20px 30px;
            border-top: 1px solid var(--border-color);
            display: flex;
            justify-content: flex-end;
            gap: 12px;
        }

        .modal-footer button {
            padding: 12px 28px;
            border-radius: 8px;
            font-size: 14px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s;
        }

        .modal-footer .cancel-btn {
            background: var(--bg-light);
            border: 1px solid var(--border-color);
            color: var(--text-dark);
        }

        .modal-footer .cancel-btn:hover {
            background: #e9ecef;
        }

        .modal-footer .submit-btn {
            background: var(--primary-color);
            border: none;
            color: white;
        }

        .modal-footer .submit-btn:hover {
            background: var(--primary-dark);
        }

        /* 公告详情弹窗 */
        .announcement-modal .modal {
            max-width: 600px;
        }

        .announcement-content {
            font-size: 15px;
            line-height: 1.8;
            color: var(--text-dark);
            white-space: pre-wrap;
        }

        /* 用户管理 */
        .user-list {
            display: grid;
            gap: 16px;
        }

        .user-item {
            background: var(--bg-white);
            border-radius: 12px;
            padding: 20px 25px;
            box-shadow: var(--shadow);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .user-item-info {
            display: flex;
            align-items: center;
            gap: 16px;
        }

        .user-item-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            font-weight: 600;
            color: white;
        }

        .user-item-avatar.admin { background: linear-gradient(135deg, var(--primary-color), var(--primary-light)); }
        .user-item-avatar.employee { background: linear-gradient(135deg, var(--secondary-color), #74b9ff); }

        .user-item-details h4 {
            font-size: 16px;
            color: var(--text-dark);
            margin-bottom: 4px;
        }

        .user-item-details p {
            font-size: 13px;
            color: var(--text-light);
        }

        .user-role-badge {
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 13px;
            font-weight: 500;
        }

        .user-role-badge.admin {
            background: rgba(30, 90, 168, 0.1);
            color: var(--primary-color);
        }

        .user-role-badge.employee {
            background: rgba(74, 144, 217, 0.1);
            color: var(--secondary-color);
        }

        /* 空状态 */
        .empty-state {
            text-align: center;
            padding: 60px 20px;
            color: var(--text-light);
        }

        .empty-state .icon {
            font-size: 60px;
            margin-bottom: 20px;
            opacity: 0.5;
        }

        .empty-state h4 {
            font-size: 18px;
            margin-bottom: 8px;
            color: var(--text-dark);
        }

        /* 响应式 */
        @media (max-width: 768px) {
            .sidebar {
                width: 80px;
            }

            .menu-item span:not(.icon) {
                display: none;
            }

            .menu-item {
                justify-content: center;
                padding: 14px;
            }

            .menu-item .icon {
                margin: 0;
            }

            .nav-brand h1 {
                display: none;
            }

            .main-content {
                padding: 20px;
            }

            .content-grid {
                grid-template-columns: 1fr;
            }

            .module-list {
                grid-template-columns: 1fr;
            }

            .doc-item {
                flex-direction: column;
                align-items: flex-start;
                gap: 15px;
            }

            .doc-actions {
                width: 100%;
            }

            .doc-actions button {
                flex: 1;
            }
        }

        /* 统计卡片 */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .stat-card {
            background: var(--bg-white);
            border-radius: 12px;
            padding: 24px;
            box-shadow: var(--shadow);
        }

        .stat-card .stat-icon {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            margin-bottom: 15px;
        }

        .stat-card .stat-value {
            font-size: 32px;
            font-weight: 700;
            color: var(--text-dark);
            margin-bottom: 5px;
        }

        .stat-card .stat-label {
            font-size: 14px;
            color: var(--text-light);
        }

        /* 确认弹窗 */
        .confirm-modal .modal {
            max-width: 400px;
            text-align: center;
        }

        .confirm-modal .modal-body {
            padding: 40px 30px;
        }

        .confirm-modal .confirm-icon {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: rgba(231, 76, 60, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
            color: var(--danger-color);
            margin: 0 auto 20px;
        }

        .confirm-modal h3 {
            font-size: 20px;
            margin-bottom: 10px;
        }

        .confirm-modal p {
            color: var(--text-light);
            margin-bottom: 25px;
        }

        .confirm-modal .modal-footer {
            justify-content: center;
        }

        .confirm-modal .delete-btn {
            background: var(--danger-color);
            color: white;
            border: none;
        }

        .confirm-modal .delete-btn:hover {
            background: #c0392b;
        }

        /* Toast 提示 */
        .toast {
            position: fixed;
            bottom: 30px;
            right: 30px;
            padding: 16px 24px;
            background: var(--text-dark);
            color: white;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            z-index: 3000;
            animation: toastIn 0.3s ease;
        }

        .toast.success {
            background: var(--success-color);
        }

        .toast.error {
            background: var(--danger-color);
        }

        @keyframes toastIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .toast.hide {
            animation: toastOut 0.3s ease forwards;
        }

        @keyframes toastOut {
            to {
                opacity: 0;
                transform: translateY(20px);
            }
        }
    </style>
</head>
<body>
    <!-- 登录页面 -->
    <div class="login-container" id="loginPage">
        <div class="login-box">
            <div class="login-header">
                <div class="logo">🏢</div>
                <h1>深圳市捷希科技有限公司</h1>
                <p>企业内部管理系统</p>
            </div>
            <form class="login-form" id="loginForm">
                <div class="form-group">
                    <label>账号</label>
                    <input type="text" id="loginAccount" placeholder="请输入账号" required>
                </div>
                <div class="form-group">
                    <label>密码</label>
                    <input type="password" id="loginPassword" placeholder="请输入密码" required>
                </div>
                <div class="error-msg" id="loginError">账号或密码错误</div>
                <button type="submit" class="login-btn">登 录</button>
            </form>
            <div class="login-footer">
                <p>© 2024 深圳市捷希科技有限公司</p>
                <div class="demo-accounts">
                    <h4>测试账号</h4>
                    <p>管理员：<code>admin</code> / <code>admin123</code></p>
                    <p>员工：<code>user</code> / <code>user123</code></p>
                </div>
            </div>
        </div>
    </div>

    <!-- 主系统 -->
    <div class="main-system" id="mainSystem">
        <!-- 顶部导航 -->
        <nav class="top-nav">
            <div class="nav-brand">
                <div class="logo-icon">🏢</div>
                <h1>捷希科技内部系统</h1>
            </div>
            <div class="nav-user">
                <div class="user-info" onclick="showUserInfo()">
                    <div class="user-avatar" id="userAvatar">U</div>
                    <div>
                        <div class="user-name" id="userName">用户</div>
                        <div class="user-role" id="userRole">员工</div>
                    </div>
                </div>
                <button class="logout-btn" onclick="logout()">退出登录</button>
            </div>
        </nav>

        <div class="main-layout">
            <!-- 侧边栏 -->
            <aside class="sidebar">
                <ul class="sidebar-menu">
                    <li class="menu-item active" data-page="dashboard">
                        <span class="icon">📊</span>
                        <span>工作台</span>
                    </li>
                    <li class="menu-item" data-page="training">
                        <span class="icon">📚</span>
                        <span>培训资料</span>
                    </li>
                    <li class="menu-item" data-page="business">
                        <span class="icon">📋</span>
                        <span>业务流程</span>
                    </li>
                    <li class="menu-item" data-page="announcement">
                        <span class="icon">📢</span>
                        <span>公告通知</span>
                    </li>
                    <div class="menu-divider admin-only"></div>
                    <li class="menu-item admin-only" data-page="userManagement">
                        <span class="icon">👥</span>
                        <span>用户管理</span>
                    </li>
                </ul>
            </aside>

            <!-- 主内容区 -->
            <main class="main-content" id="mainContent">
                <!-- 工作台 -->
                <div class="page-content" id="page-dashboard">
                    <div class="page-header">
                        <h2>工作台</h2>
                        <p>欢迎使用深圳市捷希科技有限公司内部管理系统</p>
                    </div>

                    <div class="announcement-section" id="announcementBanner">
                        <div class="announcement-header">
                            <h3>📢 最新公告</h3>
                        </div>
                        <div class="announcement-list" id="announcementBannerList">
                            <!-- 动态渲染 -->
                        </div>
                    </div>

                    <div class="stats-grid">
                        <div class="stat-card">
                            <div class="stat-icon" style="background: linear-gradient(135deg, #667eea, #764ba2);">📚</div>
                            <div class="stat-value" id="statTraining">0</div>
                            <div class="stat-label">培训资料</div>
                        </div>
                        <div class="stat-card">
                            <div class="stat-icon" style="background: linear-gradient(135deg, #43e97b, #38f9d7);">📋</div>
                            <div class="stat-value" id="statBusiness">0</div>
                            <div class="stat-label">业务流程</div>
                        </div>
                        <div class="stat-card">
                            <div class="stat-icon" style="background: linear-gradient(135deg, #fa709a, #fee140);">📢</div>
                            <div class="stat-value" id="statAnnouncement">0</div>
                            <div class="stat-label">公告通知</div>
                        </div>
                    </div>

                    <div class="content-grid">
                        <div class="content-card" onclick="switchPage('training')">
                            <div class="card-header">
                                <div class="card-icon training">📚</div>
                                <span class="card-count" id="cardTrainingCount">0 篇</span>
                            </div>
                            <h3 class="card-title">培训资料</h3>
                            <p class="card-desc">查看入职培训、岗位培训、技能培训等各类学习资料</p>
                        </div>
                        <div class="content-card" onclick="switchPage('business')">
                            <div class="card-header">
                                <div class="card-icon business">📋</div>
                                <span class="card-count" id="cardBusinessCount">0 篇</span>
                            </div>
                            <h3 class="card-title">业务流程</h3>
                            <p class="card-desc">查看项目、产品、商务、设计等各业务模块流程文档</p>
                        </div>
                    </div>
                </div>

                <!-- 培训资料 -->
                <div class="page-content" id="page-training" style="display:none;">
                    <div class="page-header">
                        <h2>培训资料</h2>
                        <p>管理公司各类培训资料，提升员工专业技能</p>
                    </div>
                    <div class="module-list" id="trainingModuleList">
                        <!-- 动态渲染 -->
                    </div>
                </div>

                <!-- 业务流程 -->
                <div class="page-content" id="page-business" style="display:none;">
                    <div class="page-header">
                        <h2>业务流程</h2>
                        <p>规范业务流程，提高工作效率</p>
                    </div>
                    <div class="module-list" id="businessModuleList">
                        <!-- 动态渲染 -->
                    </div>
                </div>

                <!-- 公告通知 -->
                <div class="page-content" id="page-announcement" style="display:none;">
                    <div class="page-header">
                        <h2>公告通知</h2>
                        <p>查看公司发布的各类公告和通知</p>
                    </div>
                    <div class="detail-header">
                        <button class="add-btn admin-only" onclick="openAnnouncementModal()">
                            ➕ 发布公告
                        </button>
                    </div>
                    <div class="doc-list" id="announcementList">
                        <!-- 动态渲染 -->
                    </div>
                </div>

                <!-- 用户管理 -->
                <div class="page-content" id="page-userManagement" style="display:none;">
                    <div class="page-header">
                        <h2>用户管理</h2>
                        <p>管理系统用户账号和权限</p>
                    </div>
                    <div class="user-list" id="userList">
                        <!-- 动态渲染 -->
                    </div>
                </div>

                <!-- 培训详情页 -->
                <div class="detail-page" id="detail-training">
                    <div class="detail-header">
                        <button class="back-btn" onclick="closeDetail('training')">← 返回</button>
                        <button class="add-btn admin-only" onclick="openDocModal('training')">➕ 添加资料</button>
                    </div>
                    <h2 id="detail-training-title" style="margin-bottom: 20px;">培训资料</h2>
                    <div class="doc-list" id="detail-training-list">
                        <!-- 动态渲染 -->
                    </div>
                </div>

                <!-- 业务详情页 -->
                <div class="detail-page" id="detail-business">
                    <div class="detail-header">
                        <button class="back-btn" onclick="closeDetail('business')">← 返回</button>
                        <button class="add-btn admin-only" onclick="openDocModal('business')">➕ 添加文档</button>
                    </div>
                    <h2 id="detail-business-title" style="margin-bottom: 20px;">业务流程</h2>
                    <div class="doc-list" id="detail-business-list">
                        <!-- 动态渲染 -->
                    </div>
                </div>
            </main>
        </div>
    </div>

    <!-- 文档弹窗 -->
    <div class="modal-overlay" id="docModal">
        <div class="modal">
            <div class="modal-header">
                <h3 id="docModalTitle">添加文档</h3>
                <button class="modal-close" onclick="closeDocModal()">×</button>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label>文档标题</label>
                    <input type="text" id="docTitle" placeholder="请输入文档标题">
                </div>
                <div class="form-group">
                    <label>文档类型</label>
                    <select id="docType">
                        <!-- 动态渲染 -->
                    </select>
                </div>
                <div class="form-group">
                    <label>文档描述</label>
                    <textarea id="docDesc" placeholder="请输入文档描述或内容"></textarea>
                </div>
                <input type="hidden" id="editDocId">
            </div>
            <div class="modal-footer">
                <button class="cancel-btn" onclick="closeDocModal()">取消</button>
                <button class="submit-btn" onclick="saveDoc()">保存</button>
            </div>
        </div>
    </div>

    <!-- 公告弹窗 -->
    <div class="modal-overlay announcement-modal" id="announcementModal">
        <div class="modal">
            <div class="modal-header">
                <h3 id="announcementModalTitle">发布公告</h3>
                <button class="modal-close" onclick="closeAnnouncementModal()">×</button>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label>公告标题</label>
                    <input type="text" id="announcementTitle" placeholder="请输入公告标题">
                </div>
                <div class="form-group">
                    <label>公告类型</label>
                    <select id="announcementType">
                        <option value="公司通知">公司通知</option>
                        <option value="活动公告">活动公告</option>
                        <option value="制度更新">制度更新</option>
                        <option value="节假日安排">节假日安排</option>
                    </select>
                </div>
                <div class="form-group">
                    <label>公告内容</label>
                    <textarea id="announcementContent" placeholder="请输入公告内容"></textarea>
                </div>
                <input type="hidden" id="editAnnouncementId">
            </div>
            <div class="modal-footer">
                <button class="cancel-btn" onclick="closeAnnouncementModal()">取消</button>
                <button class="submit-btn" onclick="saveAnnouncement()">发布</button>
            </div>
        </div>
    </div>

    <!-- 公告详情弹窗 -->
    <div class="modal-overlay announcement-modal" id="announcementDetailModal">
        <div class="modal">
            <div class="modal-header">
                <h3 id="announcementDetailTitle">公告详情</h3>
                <button class="modal-close" onclick="closeAnnouncementDetailModal()">×</button>
            </div>
            <div class="modal-body">
                <div class="announcement-content" id="announcementDetailContent"></div>
            </div>
            <div class="modal-footer">
                <button class="cancel-btn" onclick="closeAnnouncementDetailModal()">关闭</button>
            </div>
        </div>
    </div>

    <!-- 确认删除弹窗 -->
    <div class="modal-overlay confirm-modal" id="confirmModal">
        <div class="modal">
            <div class="modal-body">
                <div class="confirm-icon">⚠️</div>
                <h3>确认删除</h3>
                <p id="confirmMessage">确定要删除此项吗？此操作不可撤销。</p>
            </div>
            <div class="modal-footer">
                <button class="cancel-btn" onclick="closeConfirmModal()">取消</button>
                <button class="delete-btn" onclick="confirmDelete()">确认删除</button>
            </div>
        </div>
    </div>

    <script>
        // 数据存储键
        const STORAGE_KEYS = {
            training: 'jc_training',
            business: 'jc_business',
            announcement: 'jc_announcement',
            users: 'jc_users'
        };

        // 默认数据
        const DEFAULT_DATA = {
            users: [
                { id: 1, username: 'admin', password: 'admin123', name: '系统管理员', role: 'admin' },
                { id: 2, username: 'user', password: 'user123', name: '张明', role: 'employee' },
                { id: 3, username: 'liwei', password: 'liwei123', name: '李伟', role: 'employee' },
                { id: 4, username: 'wangfang', password: 'wang123', name: '王芳', role: 'employee' }
            ],
            training: [
                { id: 1, title: '新员工入职指南', type: 'onboarding', desc: '详细介绍公司文化、组织架构、规章制度等，帮助新员工快速融入团队。包含公司发展历程、价值观、行为准则等内容。', date: '2024-01-15', views: 156 },
                { id: 2, title: '公司产品线介绍', type: 'onboarding', desc: '全面介绍公司主要产品线、技术架构、市场定位等内容。', date: '2024-01-18', views: 98 },
                { id: 3, title: 'OA系统使用培训', type: 'onboarding', desc: '学习公司办公自动化系统的各项功能和使用方法。', date: '2024-02-01', views: 134 },
                { id: 4, title: '项目管理流程', type: 'job', desc: '详细讲解项目从立项到结项的全流程管理规范，包括需求分析、计划制定、进度跟踪、风险管理等环节。', date: '2024-01-20', views: 89 },
                { id: 5, title: '客户服务标准', type: 'job', desc: '客服岗位工作流程、服务规范、问题处理流程等培训资料。', date: '2024-02-05', views: 67 },
                { id: 6, title: '技术开发规范', type: 'skill', desc: '前端、后端、数据库开发规范文档，代码审查标准，Git使用规范等。', date: '2024-02-10', views: 145 },
                { id: 7, title: 'UI/UX设计规范', type: 'skill', desc: '设计规范文档，包括色彩体系、字体规范、组件库使用、交互设计原则等。', date: '2024-02-15', views: 112 },
                { id: 8, title: '数据分析方法', type: 'skill', desc: '数据分析工具使用、数据处理方法、报表制作技巧等培训内容。', date: '2024-02-20', views: 78 }
            ],
            business: [
                { id: 1, title: '项目立项审批流程', type: 'project', desc: '项目立项申请、审批流程、合同签订等规范文档，包含各环节审批要点和注意事项。', date: '2024-01-10', views: 201 },
                { id: 2, title: '项目进度管理规定', type: 'project', desc: '项目进度计划、跟踪、汇报的管理规定和模板。', date: '2024-01-15', views: 156 },
                { id: 3, title: '项目验收标准', type: 'project', desc: '项目交付物验收标准、验收流程、常见问题处理。', date: '2024-01-20', views: 134 },
                { id: 4, title: '产品需求文档规范', type: 'product', desc: 'PRD文档模板、写作规范、评审流程等指导文档。', date: '2024-01-12', views: 178 },
                { id: 5, title: '产品迭代管理', type: 'product', desc: '版本规划、迭代计划、发布流程等产品生命周期管理规范。', date: '2024-01-18', views: 145 },
                { id: 6, title: '客户拜访流程', type: 'business', desc: '客户拜访准备、沟通技巧、跟进要点等商务拓展指南。', date: '2024-01-08', views: 198 },
                { id: 7, title: '合同评审流程', type: 'business', desc: '合同起草、评审、签订、归档等全流程管理规定。', date: '2024-01-14', views: 167 },
                { id: 8, title: '投标工作流程', type: 'business', desc: '投标文件准备、标书制作、投标评审、中标跟进等流程。', date: '2024-01-22', views: 123 },
                { id: 9, title: '设计稿评审规范', type: 'design', desc: 'UI设计稿评审标准、评审流程、修改意见反馈机制。', date: '2024-01-16', views: 189 },
                { id: 10, title: '品牌视觉规范', type: 'design', desc: '公司VI系统、品牌标识、视觉规范等设计标准文档。', date: '2024-01-20', views: 156 }
            ],
            announcement: [
                { id: 1, title: '关于2024年春节放假的通知', type: '节假日安排', content: '各部门：根据国家法定节假日规定，结合公司实际情况，现将2024年春节放假安排通知如下：\n\n一、放假时间：2月9日（除夕）至2月17日（正月初八），共9天。2月18日（正月初九）正常上班。\n\n二、值班安排：各部门需安排人员值班，确保紧急事务及时处理。\n\n三、安全须知：放假前请各部门检查办公区域安全隐患，关闭电源门窗。\n\n四、祝福语：恭祝全体员工新春快乐，阖家幸福！', date: '2024-01-25', views: 456 },
                { id: 2, title: '公司新官网正式上线公告', type: '公司通知', content: '各位同事：\n\n经过数月的精心策划和开发，深圳市捷希科技有限公司官方网站（PC端+移动端）现已正式上线！\n\n新网站采用全新设计理念，全面展示了公司产品、解决方案、成功案例等内容。网站地址：www.jiexi.com\n\n欢迎大家访问并提出宝贵意见！', date: '2024-01-20', views: 328 },
                { id: 3, title: '2024年度团建活动通知', type: '活动公告', content: '为增强团队凝聚力，促进同事间的沟通与交流，公司决定于3月份组织年度团建活动。\n\n活动地点：待定（根据投票结果确定）\n活动人数：全体员工\n活动内容：户外拓展、团队游戏、自助烧烤等\n\n请各部门合理安排工作，届时积极参与。具体时间和安排另行通知。', date: '2024-02-01', views: 289 },
                { id: 4, title: '考勤管理制度更新通知', type: '制度更新', content: '各位同事：\n\n为规范公司考勤管理，现对《考勤管理制度》进行部分修订，主要调整如下：\n\n1. 上班时间调整为9:00，下班时间调整为18:00\n2. 午休时间调整为12:00-13:00\n3. 忘打卡每月有3次补录机会\n4. 请假审批流程优化，部门经理可直接审批3天以内假期\n\n新制度自2024年3月1日起执行。', date: '2024-02-10', views: 345 }
            ]
        };

        // 模块配置
        const TRAINING_MODULES = [
            { type: 'onboarding', name: '入职培训', icon: 'onboarding', desc: '新员工入职必读' },
            { type: 'job', name: '岗位培训', icon: 'job', desc: '岗位职责与技能' },
            { type: 'skill', name: '技能培训', icon: 'skill', desc: '专业技能提升' }
        ];

        const BUSINESS_MODULES = [
            { type: 'project', name: '项目流程', icon: 'project', desc: '项目管理规范' },
            { type: 'product', name: '产品流程', icon: 'product', desc: '产品管理规范' },
            { type: 'business', name: '商务流程', icon: 'business-doc', desc: '商务合作规范' },
            { type: 'design', name: '设计流程', icon: 'design', desc: '设计工作规范' }
        ];

        // 当前状态
        let currentUser = null;
        let currentDetailType = null;
        let deleteCallback = null;

        // 初始化
        document.addEventListener('DOMContentLoaded', function() {
            initData();
            checkLoginStatus();
            bindEvents();
        });

        // 初始化数据
        function initData() {
            Object.keys(STORAGE_KEYS).forEach(key => {
                const localData = localStorage.getItem(STORAGE_KEYS[key]);
                if (!localData) {
                    localStorage.setItem(STORAGE_KEYS[key], JSON.stringify(DEFAULT_DATA[key]));
                }
            });
        }

        // 检查登录状态
        function checkLoginStatus() {
            const savedUser = localStorage.getItem('jc_current_user');
            if (savedUser) {
                currentUser = JSON.parse(savedUser);
                showMainSystem();
            }
        }

        // 绑定事件
        function bindEvents() {
            // 登录表单
            document.getElementById('loginForm').addEventListener('submit', handleLogin);
            
            // 侧边栏菜单
            document.querySelectorAll('.menu-item').forEach(item => {
                item.addEventListener('click', function() {
                    const page = this.dataset.page;
                    if (page) switchPage(page);
                });
            });
        }

        // 登录处理
        function handleLogin(e) {
            e.preventDefault();
            const account = document.getElementById('loginAccount').value;
            const password = document.getElementById('loginPassword').value;
            
            const users = JSON.parse(localStorage.getItem(STORAGE_KEYS.users));
            const user = users.find(u => u.username === account && u.password === password);
            
            if (user) {
                currentUser = user;
                localStorage.setItem('jc_current_user', JSON.stringify(user));
                document.getElementById('loginError').style.display = 'none';
                showMainSystem();
                showToast('登录成功！', 'success');
            } else {
                document.getElementById('loginError').style.display = 'block';
            }
        }

        // 退出登录
        function logout() {
            currentUser = null;
            localStorage.removeItem('jc_current_user');
            document.getElementById('loginPage').style.display = 'flex';
            document.getElementById('mainSystem').style.display = 'none';
            document.getElementById('loginAccount').value = '';
            document.getElementById('loginPassword').value = '';
            showToast('已退出登录');
        }

        // 显示主系统
        function showMainSystem() {
            document.getElementById('loginPage').style.display = 'none';
            document.getElementById('mainSystem').style.display = 'block';
            
            // 更新用户信息
            document.getElementById('userName').textContent = currentUser.name;
            document.getElementById('userRole').textContent = currentUser.role === 'admin' ? '管理员' : '员工';
            document.getElementById('userAvatar').textContent = currentUser.name.charAt(0);
            
            // 设置管理员视图
            if (currentUser.role === 'admin') {
                document.body.classList.add('is-admin');
            } else {
                document.body.classList.remove('is-admin');
            }
            
            // 加载首页数据
            switchPage('dashboard');
        }

        // 切换页面
        function switchPage(page) {
            // 更新菜单状态
            document.querySelectorAll('.menu-item').forEach(item => {
                item.classList.remove('active');
                if (item.dataset.page === page) {
                    item.classList.add('active');
                }
            });
            
            // 隐藏所有页面
            document.querySelectorAll('.page-content, .detail-page').forEach(p => {
                p.style.display = 'none';
            });
            
            // 显示目标页面
            const targetPage = document.getElementById('page-' + page);
            if (targetPage) {
                targetPage.style.display = 'block';
                loadPageData(page);
            }
        }

        // 加载页面数据
        function loadPageData(page) {
            switch(page) {
                case 'dashboard':
                    loadDashboard();
                    break;
                case 'training':
                    loadTrainingModules();
                    break;
                case 'business':
                    loadBusinessModules();
                    break;
                case 'announcement':
                    loadAnnouncements();
                    break;
                case 'userManagement':
                    loadUsers();
                    break;
            }
        }

        // 加载工作台数据
        function loadDashboard() {
            const training = JSON.parse(localStorage.getItem(STORAGE_KEYS.training));
            const business = JSON.parse(localStorage.getItem(STORAGE_KEYS.business));
            const announcement = JSON.parse(localStorage.getItem(STORAGE_KEYS.announcement));
            
            // 统计数据
            document.getElementById('statTraining').textContent = training.length;
            document.getElementById('statBusiness').textContent = business.length;
            document.getElementById('statAnnouncement').textContent = announcement.length;
            document.getElementById('cardTrainingCount').textContent = training.length + ' 篇';
            document.getElementById('cardBusinessCount').textContent = business.length + ' 篇';
            
            // 最新公告
            const bannerList = document.getElementById('announcementBannerList');
            const latestAnnouncements = announcement.slice(0, 3);
            bannerList.innerHTML = latestAnnouncements.map(item => `
                <div class="announcement-item" onclick="viewAnnouncement(${item.id})">
                    <div class="announcement-content">
                        <div class="announcement-title">${item.title}</div>
                        <div class="announcement-time">${item.date}</div>
                    </div>
                    <span class="announcement-tag">${item.type}</span>
                </div>
            `).join('');
        }

        // 加载培训模块
        function loadTrainingModules() {
            const training = JSON.parse(localStorage.getItem(STORAGE_KEYS.training));
            const moduleList = document.getElementById('trainingModuleList');
            
            moduleList.innerHTML = TRAINING_MODULES.map(module => {
                const count = training.filter(t => t.type === module.type).length;
                return `
                    <div class="module-item" onclick="showTrainingDetail('${module.type}')">
                        <div class="module-icon ${module.icon}">${getModuleIcon(module.type)}</div>
                        <h3 class="module-title">${module.name}</h3>
                        <p class="module-count">${count} 篇资料</p>
                    </div>
                `;
            }).join('');
        }

        // 加载业务流程模块
        function loadBusinessModules() {
            const business = JSON.parse(localStorage.getItem(STORAGE_KEYS.business));
            const moduleList = document.getElementById('businessModuleList');
            
            moduleList.innerHTML = BUSINESS_MODULES.map(module => {
                const count = business.filter(b => b.type === module.type).length;
                return `
                    <div class="module-item" onclick="showBusinessDetail('${module.type}')">
                        <div class="module-icon ${module.icon}">${getModuleIcon(module.type)}</div>
                        <h3 class="module-title">${module.name}</h3>
                        <p class="module-count">${count} 篇文档</p>
                    </div>
                `;
            }).join('');
        }

        // 获取模块图标
        function getModuleIcon(type) {
            const icons = {
                'onboarding': '👋',
                'job': '💼',
                'skill': '🎯',
                'project': '📁',
                'product': '📦',
                'business': '🤝',
                'design': '🎨'
            };
            return icons[type] || '📄';
        }

        // 显示培训详情
        function showTrainingDetail(type) {
            currentDetailType = type;
            const training = JSON.parse(localStorage.getItem(STORAGE_KEYS.training));
            const docs = training.filter(t => t.type === type);
            
            const module = TRAINING_MODULES.find(m => m.type === type);
            document.getElementById('detail-training-title').textContent = module ? module.name : '培训资料';
            
            const list = document.getElementById('detail-training-list');
            if (docs.length === 0) {
                list.innerHTML = `
                    <div class="empty-state">
                        <div class="icon">📭</div>
                        <h4>暂无资料</h4>
                        <p>该分类下还没有培训资料</p>
                    </div>
                `;
            } else {
                list.innerHTML = docs.map(doc => `
                    <div class="doc-item">
                        <div class="doc-info">
                            <div class="doc-icon">📄</div>
                            <div class="doc-details">
                                <h4>${doc.title}</h4>
                                <div class="doc-meta">
                                    <span>📅 ${doc.date}</span>
                                    <span>👁️ ${doc.views} 次浏览</span>
                                </div>
                            </div>
                        </div>
                        <div class="doc-actions ${currentUser.role !== 'admin' ? 'hidden' : ''}">
                            <button class="edit-btn" onclick="editDoc('training', ${doc.id})">编辑</button>
                            <button class="delete-btn" onclick="deleteDoc('training', ${doc.id})">删除</button>
                        </div>
                    </div>
                `).join('');
            }
            
            document.getElementById('detail-training').style.display = 'block';
            document.querySelectorAll('.page-content').forEach(p => p.style.display = 'none');
        }

        // 显示业务详情
        function showBusinessDetail(type) {
            currentDetailType = type;
            const business = JSON.parse(localStorage.getItem(STORAGE_KEYS.business));
            const docs = business.filter(b => b.type === type);
            
            const module = BUSINESS_MODULES.find(m => m.type === type);
            document.getElementById('detail-business-title').textContent = module ? module.name : '业务流程';
            
            const list = document.getElementById('detail-business-list');
            if (docs.length === 0) {
                list.innerHTML = `
                    <div class="empty-state">
                        <div class="icon">📭</div>
                        <h4>暂无文档</h4>
                        <p>该分类下还没有业务流程文档</p>
                    </div>
                `;
            } else {
                list.innerHTML = docs.map(doc => `
                    <div class="doc-item">
                        <div class="doc-info">
                            <div class="doc-icon">📋</div>
                            <div class="doc-details">
                                <h4>${doc.title}</h4>
                                <div class="doc-meta">
                                    <span>📅 ${doc.date}</span>
                                    <span>👁️ ${doc.views} 次浏览</span>
                                </div>
                            </div>
                        </div>
                        <div class="doc-actions ${currentUser.role !== 'admin' ? 'hidden' : ''}">
                            <button class="edit-btn" onclick="editDoc('business', ${doc.id})">编辑</button>
                            <button class="delete-btn" onclick="deleteDoc('business', ${doc.id})">删除</button>
                        </div>
                    </div>
                `).join('');
            }
            
            document.getElementById('detail-business').style.display = 'block';
            document.querySelectorAll('.page-content').forEach(p => p.style.display = 'none');
        }

        // 关闭详情页
        function closeDetail(type) {
            document.getElementById('detail-' + type).style.display = 'none';
            switchPage(type);
        }

        // 打开文档弹窗
        function openDocModal(type) {
            document.getElementById('editDocId').value = '';
            document.getElementById('docTitle').value = '';
            document.getElementById('docDesc').value = '';
            document.getElementById('docType').value = currentDetailType;
            
            // 设置类型选项
            const modules = type === 'training' ? TRAINING_MODULES : BUSINESS_MODULES;
            document.getElementById('docType').innerHTML = modules.map(m => 
                `<option value="${m.type}">${m.name}</option>`
            ).join('');
            document.getElementById('docType').value = currentDetailType;
            
            document.getElementById('docModalTitle').textContent = '添加文档';
            document.getElementById('docModal').classList.add('active');
        }

        // 关闭文档弹窗
        function closeDocModal() {
            document.getElementById('docModal').classList.remove('active');
        }

        // 编辑文档
        function editDoc(type, id) {
            const key = type === 'training' ? STORAGE_KEYS.training : STORAGE_KEYS.business;
            const data = JSON.parse(localStorage.getItem(key));
            const doc = data.find(d => d.id === id);
            
            if (doc) {
                document.getElementById('editDocId').value = id;
                document.getElementById('docTitle').value = doc.title;
                document.getElementById('docDesc').value = doc.desc;
                document.getElementById('docType').value = doc.type;
                
                const modules = type === 'training' ? TRAINING_MODULES : BUSINESS_MODULES;
                document.getElementById('docType').innerHTML = modules.map(m => 
                    `<option value="${m.type}">${m.name}</option>`
                ).join('');
                document.getElementById('docType').value = doc.type;
                
                document.getElementById('docModalTitle').textContent = '编辑文档';
                document.getElementById('docModal').classList.add('active');
            }
        }

        // 保存文档
        function saveDoc() {
            const title = document.getElementById('docTitle').value.trim();
            const desc = document.getElementById('docDesc').value.trim();
            const type = document.getElementById('docType').value;
            const editId = document.getElementById('editDocId').value;
            
            if (!title) {
                showToast('请输入文档标题', 'error');
                return;
            }
            
            const key = currentPageType === 'training' ? STORAGE_KEYS.training : STORAGE_KEYS.business;
            let data = JSON.parse(localStorage.getItem(key));
            
            if (editId) {
                // 编辑
                const index = data.findIndex(d => d.id === parseInt(editId));
                if (index !== -1) {
                    data[index].title = title;
                    data[index].desc = desc;
                    data[index].type = type;
                }
                showToast('文档已更新', 'success');
            } else {
                // 新增
                const newId = Math.max(...data.map(d => d.id)) + 1;
                data.push({
                    id: newId,
                    title: title,
                    type: type,
                    desc: desc,
                    date: new Date().toISOString().split('T')[0],
                    views: 0
                });
                showToast('文档已添加', 'success');
            }
            
            localStorage.setItem(key, JSON.stringify(data));
            closeDocModal();
            
            // 刷新当前视图
            if (currentDetailType) {
                showTrainingDetail(currentDetailType);
            } else {
                loadPageData(currentPageType);
            }
        }

        // 删除文档
        function deleteDoc(type, id) {
            document.getElementById('confirmMessage').textContent = '确定要删除此文档吗？此操作不可撤销。';
            deleteCallback = () => {
                const key = type === 'training' ? STORAGE_KEYS.training : STORAGE_KEYS.business;
                let data = JSON.parse(localStorage.getItem(key));
                data = data.filter(d => d.id !== id);
                localStorage.setItem(key, JSON.stringify(data));
                showToast('文档已删除', 'success');
                
                if (currentDetailType) {
                    showTrainingDetail(currentDetailType);
                } else {
                    loadPageData(type);
                }
            };
            document.getElementById('confirmModal').classList.add('active');
        }

        // 加载公告列表
        function loadAnnouncements() {
            const announcement = JSON.parse(localStorage.getItem(STORAGE_KEYS.announcement));
            const list = document.getElementById('announcementList');
            
            if (announcement.length === 0) {
                list.innerHTML = `
                    <div class="empty-state">
                        <div class="icon">📭</div>
                        <h4>暂无公告</h4>
                        <p>暂无发布的公告通知</p>
                    </div>
                `;
            } else {
                list.innerHTML = announcement.map(item => `
                    <div class="doc-item">
                        <div class="doc-info">
                            <div class="doc-icon" style="background: linear-gradient(135deg, #fa709a, #fee140);">📢</div>
                            <div class="doc-details">
                                <h4>${item.title}</h4>
                                <div class="doc-meta">
                                    <span>🏷️ ${item.type}</span>
                                    <span>📅 ${item.date}</span>
                                    <span>👁️ ${item.views} 次浏览</span>
                                </div>
                            </div>
                        </div>
                        <div class="doc-actions ${currentUser.role !== 'admin' ? 'hidden' : ''}">
                            <button class="view-btn" onclick="viewAnnouncement(${item.id})">查看</button>
                            <button class="edit-btn" onclick="editAnnouncement(${item.id})">编辑</button>
                            <button class="delete-btn" onclick="deleteAnnouncement(${item.id})">删除</button>
                        </div>
                    </div>
                `).join('');
            }
        }

        // 打开公告弹窗
        function openAnnouncementModal() {
            document.getElementById('editAnnouncementId').value = '';
            document.getElementById('announcementTitle').value = '';
            document.getElementById('announcementContent').value = '';
            document.getElementById('announcementType').value = '公司通知';
            document.getElementById('announcementModalTitle').textContent = '发布公告';
            document.getElementById('announcementModal').classList.add('active');
        }

        // 关闭公告弹窗
        function closeAnnouncementModal() {
            document.getElementById('announcementModal').classList.remove('active');
        }

        // 编辑公告
        function editAnnouncement(id) {
            const announcement = JSON.parse(localStorage.getItem(STORAGE_KEYS.announcement));
            const item = announcement.find(a => a.id === id);
            
            if (item) {
                document.getElementById('editAnnouncementId').value = id;
                document.getElementById('announcementTitle').value = item.title;
                document.getElementById('announcementContent').value = item.content;
                document.getElementById('announcementType').value = item.type;
                document.getElementById('announcementModalTitle').textContent = '编辑公告';
                document.getElementById('announcementModal').classList.add('active');
            }
        }

        // 保存公告
        function saveAnnouncement() {
            const title = document.getElementById('announcementTitle').value.trim();
            const content = document.getElementById('announcementContent').value.trim();
            const type = document.getElementById('announcementType').value;
            const editId = document.getElementById('editAnnouncementId').value;
            
            if (!title || !content) {
                showToast('请填写完整信息', 'error');
                return;
            }
            
            let data = JSON.parse(localStorage.getItem(STORAGE_KEYS.announcement));
            
            if (editId) {
                const index = data.findIndex(d => d.id === parseInt(editId));
                if (index !== -1) {
                    data[index].title = title;
                    data[index].content = content;
                    data[index].type = type;
                }
                showToast('公告已更新', 'success');
            } else {
                const newId = Math.max(...data.map(d => d.id)) + 1;
                data.unshift({
                    id: newId,
                    title: title,
                    content: content,
                    type: type,
                    date: new Date().toISOString().split('T')[0],
                    views: 0
                });
                showToast('公告已发布', 'success');
            }
            
            localStorage.setItem(STORAGE_KEYS.announcement, JSON.stringify(data));
            closeAnnouncementModal();
            loadAnnouncements();
        }

        // 删除公告
        function deleteAnnouncement(id) {
            document.getElementById('confirmMessage').textContent = '确定要删除此公告吗？此操作不可撤销。';
            deleteCallback = () => {
                let data = JSON.parse(localStorage.getItem(STORAGE_KEYS.announcement));
                data = data.filter(d => d.id !== id);
                localStorage.setItem(STORAGE_KEYS.announcement, JSON.stringify(data));
                showToast('公告已删除', 'success');
                loadAnnouncements();
            };
            document.getElementById('confirmModal').classList.add('active');
        }

        // 查看公告详情
        function viewAnnouncement(id) {
            const announcement = JSON.parse(localStorage.getItem(STORAGE_KEYS.announcement));
            const item = announcement.find(a => a.id === id);
            
            if (item) {
                document.getElementById('announcementDetailTitle').textContent = item.title;
                document.getElementById('announcementDetailContent').textContent = item.content;
                document.getElementById('announcementDetailModal').classList.add('active');
                
                // 更新浏览次数
                item.views++;
                localStorage.setItem(STORAGE_KEYS.announcement, JSON.stringify(announcement));
            }
        }

        // 关闭公告详情弹窗
        function closeAnnouncementDetailModal() {
            document.getElementById('announcementDetailModal').classList.remove('active');
        }

        // 加载用户列表
        function loadUsers() {
            const users = JSON.parse(localStorage.getItem(STORAGE_KEYS.users));
            const list = document.getElementById('userList');
            
            list.innerHTML = users.map(user => `
                <div class="user-item">
                    <div class="user-item-info">
                        <div class="user-item-avatar ${user.role}">${user.name.charAt(0)}</div>
                        <div class="user-item-details">
                            <h4>${user.name}</h4>
                            <p>账号：${user.username}</p>
                        </div>
                    </div>
                    <span class="user-role-badge ${user.role}">${user.role === 'admin' ? '管理员' : '员工'}</span>
                </div>
            `).join('');
        }

        // 确认删除弹窗
        function closeConfirmModal() {
            document.getElementById('confirmModal').classList.remove('active');
            deleteCallback = null;
        }

        function confirmDelete() {
            if (deleteCallback) {
                deleteCallback();
            }
            closeConfirmModal();
        }

        // 显示用户信息
        function showUserInfo() {
            showToast(`当前用户：${currentUser.name}（${currentUser.role === 'admin' ? '管理员' : '员工'}）`);
        }

        // Toast提示
        function showToast(message, type = '') {
            const existing = document.querySelector('.toast');
            if (existing) existing.remove();
            
            const toast = document.createElement('div');
            toast.className = `toast ${type}`;
            toast.textContent = message;
            document.body.appendChild(toast);
            
            setTimeout(() => {
                toast.classList.add('hide');
                setTimeout(() => toast.remove(), 300);
            }, 2500);
        }

        // 当前页面类型
        let currentPageType = '';
        
        // 重写switchPage以跟踪类型
        const originalSwitchPage = switchPage;
        switchPage = function(page) {
            currentPageType = page;
            originalSwitchPage(page);
        };
    </script>
</body>
</html>

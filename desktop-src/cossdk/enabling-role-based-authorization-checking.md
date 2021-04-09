---
description: Para usar la seguridad basada en roles en la aplicación COM+, primero debe habilitar la comprobación de la autorización basada en roles para la aplicación.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Habilitar la comprobación de la autorización de Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080234"
---
# <a name="enabling-role-based-authorization-checking"></a><span data-ttu-id="2bde8-103">Habilitar la comprobación de la autorización de Role-Based</span><span class="sxs-lookup"><span data-stu-id="2bde8-103">Enabling Role-Based Authorization Checking</span></span>

<span data-ttu-id="2bde8-104">Para usar la seguridad basada en roles en la aplicación COM+, primero debe habilitar la comprobación de la autorización basada en roles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2bde8-104">To use role-based security in your COM+ application, you must first enable role-based authorization checking for the application.</span></span> <span data-ttu-id="2bde8-105">Esto garantiza que los usuarios que tienen acceso a la aplicación se comprueban para el rol al que pertenecen antes de que estén autorizados para realizar cualquier acción en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2bde8-105">This ensures that users who are accessing the application are checked for the role they belong to before they are authorized to do anything in the application.</span></span> <span data-ttu-id="2bde8-106">Si la comprobación de la autorización basada en roles no está habilitada, no se utiliza la seguridad basada en roles de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2bde8-106">If role-based authorization checking is not enabled, role-based security for the application is not used.</span></span>

<span data-ttu-id="2bde8-107">**Para habilitar la comprobación de la autorización basada en roles**</span><span class="sxs-lookup"><span data-stu-id="2bde8-107">**To enable role-based authorization checking**</span></span>

1.  <span data-ttu-id="2bde8-108">Haga clic con el botón secundario en la aplicación COM+ para la que va a habilitar la comprobación de la autorización basada en roles y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="2bde8-108">Right-click the COM+ application for which you are enabling role-based authorization checking, and then click **Properties**.</span></span>

2.  <span data-ttu-id="2bde8-109">En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="2bde8-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="2bde8-110">En **autorización**, active la casilla **exigir comprobaciones de acceso para esta aplicación** ; la desactivación de la casilla significa que la seguridad basada en roles no se utiliza para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2bde8-110">Under **Authorization**, select the **Enforce access checks for this application** check box; clearing the check box means that role-based security is not used for the application.</span></span>

4.  <span data-ttu-id="2bde8-111">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="2bde8-111">Click **OK**.</span></span>

<span data-ttu-id="2bde8-112">La configuración de autorización seleccionada tendrá efecto la próxima vez que se inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2bde8-112">The selected authorization setting takes effect the next time the application is started.</span></span>

 

 




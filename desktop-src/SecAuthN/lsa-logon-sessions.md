---
description: Una sesión de inicio de sesión es una sesión informática que comienza cuando una autenticación de usuario se realiza correctamente y termina cuando el usuario cierra la sesión del sistema.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: Sesiones de inicio de sesión LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32a4912218b68c25c5c23334f7b34ef875fa318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278135"
---
# <a name="lsa-logon-sessions"></a><span data-ttu-id="72529-103">Sesiones de inicio de sesión LSA</span><span class="sxs-lookup"><span data-stu-id="72529-103">LSA Logon Sessions</span></span>

<span data-ttu-id="72529-104">Una [*sesión de inicio*](../secgloss/l-gly.md) de sesión es una sesión informática que comienza cuando una autenticación de usuario se realiza correctamente y termina cuando el usuario cierra la sesión del sistema.</span><span class="sxs-lookup"><span data-stu-id="72529-104">A [*logon session*](../secgloss/l-gly.md) is a computing session that begins when a user authentication is successful and ends when the user logs off of the system.</span></span>

<span data-ttu-id="72529-105">Cuando un usuario se autentica correctamente, el paquete de autenticación crea una sesión de inicio de sesión y devuelve información a la [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) que se usa para crear un [*token*](../secgloss/t-gly.md) para el nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="72529-105">When a user is successfully authenticated, the authentication package creates a logon session and returns information to the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) that is used to create a [*token*](../secgloss/t-gly.md) for the new user.</span></span> <span data-ttu-id="72529-106">Este token incluye, entre otras cosas, un [*identificador local único*](../secgloss/l-gly.md) (LUID) para la sesión de inicio de sesión, denominado [*identificador de inicio de sesión*](../secgloss/l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="72529-106">This token includes, among other things, a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) for the logon session, called the [*logon Id*](../secgloss/l-gly.md).</span></span>

<span data-ttu-id="72529-107">Cuando se crea un token, se incrementa el [*recuento de referencias*](../secgloss/r-gly.md) de la sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="72529-107">When a token is created, the [*reference count*](../secgloss/r-gly.md) for the logon session is incremented.</span></span> <span data-ttu-id="72529-108">El recuento de referencias también se incrementa siempre que se crean copias del token para la creación de procesos, la suplantación u otros usos.</span><span class="sxs-lookup"><span data-stu-id="72529-108">The reference count is also incremented whenever copies of the token are created for process creation, impersonation, or other uses.</span></span> <span data-ttu-id="72529-109">A medida que se completan los usos de los tokens y se eliminan las copias del token, se reduce el recuento de referencias de la sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="72529-109">As token uses are completed and copies of the token are deleted, the reference count for the logon session is decremented.</span></span> <span data-ttu-id="72529-110">Cuando el recuento de referencias llega a cero, se elimina la sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="72529-110">When the reference count reaches zero, the logon session is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="72529-111">Si la autenticación no se realiza correctamente, el [*paquete de autenticación*](../secgloss/a-gly.md) no debe crear una sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="72529-111">If authentication is not successful, the [*authentication package*](../secgloss/a-gly.md) should not create a logon session.</span></span> <span data-ttu-id="72529-112">Si el paquete de autenticación debe crear una sesión de inicio de sesión antes de realizar una determinación final sobre la validez del usuario y si se produce un error en la autenticación, el paquete de autenticación debe eliminar la sesión.</span><span class="sxs-lookup"><span data-stu-id="72529-112">If the authentication package must create a logon session before making a final determination about the validity of the user, and if authentication fails, the authentication package must delete the session.</span></span>

 

 

 

---
description: Controles parentales y control de cuentas de usuario
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: Controles parentales y control de cuentas de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716039"
---
# <a name="parental-controls-and-user-account-control"></a><span data-ttu-id="5cee1-103">Controles parentales y control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="5cee1-103">Parental Controls and User Account Control</span></span>

<span data-ttu-id="5cee1-104">Control de cuentas de usuario (UAC) producirá la presencia de cuentas de usuario estándar y de administrador protegido.</span><span class="sxs-lookup"><span data-stu-id="5cee1-104">User Account Control (UAC) will result in presence of Protected Administrator and Standard User accounts.</span></span> <span data-ttu-id="5cee1-105">Un administrador protegido se ejecutará con los mismos derechos que un usuario estándar en uso normal.</span><span class="sxs-lookup"><span data-stu-id="5cee1-105">A Protected Administrator will run with the same rights as a Standard User under normal usage.</span></span> <span data-ttu-id="5cee1-106">Para las operaciones con privilegios:</span><span class="sxs-lookup"><span data-stu-id="5cee1-106">For privileged operations:</span></span>

-   <span data-ttu-id="5cee1-107">A un usuario estándar se le mostrará el cuadro de diálogo interfaz de usuario de credenciales, que requiere la entrada de un nombre de usuario y una contraseña para un administrador protegido o un administrador integrado.</span><span class="sxs-lookup"><span data-stu-id="5cee1-107">A Standard User will be shown the Credentials User Interface dialog box, which requires the input of a user name and password for a Protected Administrator or built-in Administrator.</span></span>
-   <span data-ttu-id="5cee1-108">Se mostrará un administrador protegido en el cuadro de diálogo de la interfaz de usuario de consentimiento, que requiere la selección de permitir para continuar.</span><span class="sxs-lookup"><span data-stu-id="5cee1-108">A Protected Administrator will be shown the Consent User Interface dialog box, which requires selection of Allow to proceed.</span></span>

<span data-ttu-id="5cee1-109">Es importante tener en cuenta que UAC se implementa por proceso, por lo que un proceso se ejecuta con privilegios elevados o no.</span><span class="sxs-lookup"><span data-stu-id="5cee1-109">It is important to note that UAC is implemented on a per-process basis, so a process either runs elevated or not.</span></span> <span data-ttu-id="5cee1-110">Por lo general, no es adecuado desde el punto de vista de la seguridad para ejecutar aplicaciones de gran tamaño como siempre elevado.</span><span class="sxs-lookup"><span data-stu-id="5cee1-110">Generally, it is not suitable from a security standpoint to run large applications as always elevated.</span></span> <span data-ttu-id="5cee1-111">En el caso de controles parentales, el código que debe modificar la configuración debe aislarse mediante una de las dos opciones de implementación:</span><span class="sxs-lookup"><span data-stu-id="5cee1-111">For Parental Controls, code that must modify settings should be isolated by one of two implementation options:</span></span>

1.  <span data-ttu-id="5cee1-112">Cree un pequeño ejecutable para la administración de la configuración que se marca en su manifiesto como que requiere derechos administrativos.</span><span class="sxs-lookup"><span data-stu-id="5cee1-112">Create a small executable for settings management that is marked in its manifest as requiring administrative rights.</span></span> <span data-ttu-id="5cee1-113">La invocación del archivo ejecutable hará que se muestre la interfaz de usuario del consentimiento o las credenciales antes de permitir que se ejecute el proceso.</span><span class="sxs-lookup"><span data-stu-id="5cee1-113">Invocation of the executable will cause the Consent or Credentials UI to be shown prior to allowing the process to run.</span></span>
2.  <span data-ttu-id="5cee1-114">Proporcione interfaces COM en un archivo DLL de producto que permita la invocación por documentación de UAC.</span><span class="sxs-lookup"><span data-stu-id="5cee1-114">Provide COM interfaces in a product DLL that allow for invocation per UAC documentation.</span></span> <span data-ttu-id="5cee1-115">Esto también hará que se muestre la interfaz de usuario de las credenciales o el consentimiento adecuado.</span><span class="sxs-lookup"><span data-stu-id="5cee1-115">This will also cause the appropriate Consent or Credentials UI to be shown.</span></span>

 

 




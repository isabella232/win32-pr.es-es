---
title: SRPTrustLevel
description: Establece el nivel de confianza de la Directiva de restricción de software (SRP) para las aplicaciones.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- Valor del registro SRPTrustLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418539"
---
# <a name="srptrustlevel"></a><span data-ttu-id="fc4b9-104">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="fc4b9-104">SRPTrustLevel</span></span>

<span data-ttu-id="fc4b9-105">Establece el nivel de confianza de la Directiva de restricción de software (SRP) para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-105">Sets the software restriction policy (SRP) trust level for applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="fc4b9-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="fc4b9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a><span data-ttu-id="fc4b9-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc4b9-107">Remarks</span></span>

<span data-ttu-id="fc4b9-108">Se trata de un valor de **Registro \_ DWORD** que está disponible a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-108">This is a **REG\_DWORD** value that is available starting with Windows XP.</span></span>



| <span data-ttu-id="fc4b9-109">Value</span><span class="sxs-lookup"><span data-stu-id="fc4b9-109">Value</span></span>                                 | <span data-ttu-id="fc4b9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc4b9-110">Description</span></span>                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fc4b9-111">0X0 (LEVELID más seguro no \_ \_ permitido)</span><span class="sxs-lookup"><span data-stu-id="fc4b9-111">0x0 (SAFER\_LEVELID\_DISALLOWED)</span></span>      | <span data-ttu-id="fc4b9-112">No se permite el acceso a la aplicación y los privilegios de usuario que tienen en cuenta la seguridad.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-112">The application is disallowed from accessing and security-sensitive user privileges.</span></span> |
| <span data-ttu-id="fc4b9-113">0x40000 ( \_ LEVELID seguro \_ FULLYTRUSTED)</span><span class="sxs-lookup"><span data-stu-id="fc4b9-113">0x40000 (SAFE\_LEVELID\_FULLYTRUSTED)</span></span> | <span data-ttu-id="fc4b9-114">La aplicación tiene acceso ilimitado a los privilegios del usuario.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-114">The application has unrestricted access to the user's privileges.</span></span>                    |



 

<span data-ttu-id="fc4b9-115">Si el valor de **SRPTrustLevel** no existe, se usa el valor predeterminado de LEVELID Safe no \_ \_ permitido.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-115">If the **SRPTrustLevel** value does not exist, the default value of SAFER\_LEVELID\_DISALLOWED is used.</span></span> <span data-ttu-id="fc4b9-116">Si **SRPTrustLevel** es del tipo incorrecto o está fuera del intervalo, com devuelve el error COMAdmin \_ E \_ SAFERINVALID.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-116">If **SRPTrustLevel** is of the wrong type or out of range, COM returns the error COMADMIN\_E\_SAFERINVALID.</span></span> <span data-ttu-id="fc4b9-117">Si se produce un error en la activación de cualquier orden debido a las comprobaciones de confianza de SRP, COM devuelve el error CO \_ E \_ ACTIVATIONFAILED.</span><span class="sxs-lookup"><span data-stu-id="fc4b9-117">If an activation of any sort fails because of SRP trust checks, COM returns the error CO\_E\_ACTIVATIONFAILED.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc4b9-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc4b9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc4b9-119">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="fc4b9-119">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="fc4b9-120">**SRPActivateAsActivatorChecks**</span><span class="sxs-lookup"><span data-stu-id="fc4b9-120">**SRPActivateAsActivatorChecks**</span></span>](srpactivateasactivatorchecks.md)
</dt> <dt>

[<span data-ttu-id="fc4b9-121">**SRPRunningObjectChecks**</span><span class="sxs-lookup"><span data-stu-id="fc4b9-121">**SRPRunningObjectChecks**</span></span>](srprunningobjectchecks.md)
</dt> </dl>

 

 





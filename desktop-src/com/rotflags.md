---
title: ROTFlags
description: Controla el registro de un servidor COM en la tabla de objetos en ejecución (ROT).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- Valor del registro ROTFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704617"
---
# <a name="rotflags"></a><span data-ttu-id="c149b-104">ROTFlags</span><span class="sxs-lookup"><span data-stu-id="c149b-104">ROTFlags</span></span>

<span data-ttu-id="c149b-105">Controla el registro de un servidor COM en la tabla de objetos en ejecución (ROT).</span><span class="sxs-lookup"><span data-stu-id="c149b-105">Controls the registration of a COM server in the running object table (ROT).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c149b-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="c149b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a><span data-ttu-id="c149b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c149b-107">Remarks</span></span>

<span data-ttu-id="c149b-108">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c149b-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="c149b-109">Valor de marca</span><span class="sxs-lookup"><span data-stu-id="c149b-109">Flag Value</span></span> | <span data-ttu-id="c149b-110">Constante</span><span class="sxs-lookup"><span data-stu-id="c149b-110">Constant</span></span>                        |
|------------|---------------------------------|
| <span data-ttu-id="c149b-111">0x1</span><span class="sxs-lookup"><span data-stu-id="c149b-111">0x1</span></span>        | <span data-ttu-id="c149b-112">**ROTREGFLAGS \_ ALLOWANYCLIENT**</span><span class="sxs-lookup"><span data-stu-id="c149b-112">**ROTREGFLAGS\_ALLOWANYCLIENT**</span></span> |



 

### <a name="rotregflags_allowanyclient-description"></a><span data-ttu-id="c149b-113">ROTREGFLAGS \_ ALLOWANYCLIENT Descripción</span><span class="sxs-lookup"><span data-stu-id="c149b-113">ROTREGFLAGS\_ALLOWANYCLIENT Description</span></span>

<span data-ttu-id="c149b-114">Si un servidor COM desea registrarse en la tabla ROT y permitir que cualquier cliente tenga acceso al registro, debe usar la marca **ROTFLAGS \_ ALLOWANYCLIENT** .</span><span class="sxs-lookup"><span data-stu-id="c149b-114">If a COM server wants to register in the ROT and allow any client to access the registration, it must use the **ROTFLAGS\_ALLOWANYCLIENT** flag.</span></span> <span data-ttu-id="c149b-115">Un servidor COM "activar como activador" no puede especificar **ROTFLAGS \_ ALLOWANYCLIENT** porque el administrador de control de servicios (DCOMSCM) de DCOM aplica una comprobación de suplantación de identidad en esta marca.</span><span class="sxs-lookup"><span data-stu-id="c149b-115">An "Activate As Activator" COM server cannot specify **ROTFLAGS\_ALLOWANYCLIENT** because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="c149b-116">Por lo tanto, en Windows Vista y versiones posteriores, COM agrega compatibilidad con la entrada del registro **ROTFlags** que permite al servidor estipular que los registros de la tabla Rot estén disponibles para cualquier cliente.</span><span class="sxs-lookup"><span data-stu-id="c149b-116">Therefore, in Windows Vista and later, COM adds support for the **ROTFlags** registry entry that allows the server to stipulate that its ROT registrations be made available to any client.</span></span>

<span data-ttu-id="c149b-117">La entrada debe existir en el subárbol del **\_ \_ equipo local HKEY** .</span><span class="sxs-lookup"><span data-stu-id="c149b-117">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span> <span data-ttu-id="c149b-118">Esta entrada proporciona un servidor "activar como activador" con la misma funcionalidad que **ROTFLAGS \_ ALLOWANYCLIENT** proporciona para un servidor runas.</span><span class="sxs-lookup"><span data-stu-id="c149b-118">This entry provides an "Activate As Activator" server with the same functionality that **ROTFLAGS\_ALLOWANYCLIENT** provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c149b-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c149b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c149b-120">Clave AppID</span><span class="sxs-lookup"><span data-stu-id="c149b-120">AppID Key</span></span>](appid-key.md)
</dt> <dt>

[<span data-ttu-id="c149b-121">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="c149b-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="c149b-122">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="c149b-122">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 





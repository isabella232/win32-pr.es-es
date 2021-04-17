---
title: RemoteServerName
description: Configura el cliente para solicitar que el objeto se ejecute en un equipo determinado cada vez que se llame a una función de activación para la que no se especifica una estructura COSERVERINFO.
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- Valor del registro RemoteServerName COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0634d858b04fbbdf5d3a6024dbd9fdea4ee06d99
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705047"
---
# <a name="remoteservername"></a><span data-ttu-id="0b36c-104">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="0b36c-104">RemoteServerName</span></span>

<span data-ttu-id="0b36c-105">Configura el cliente para solicitar que el objeto se ejecute en un equipo determinado cada vez que se llame a una función de activación para la que no se especifica una estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) .</span><span class="sxs-lookup"><span data-stu-id="0b36c-105">Configures the client to request the object be run at a particular computer whenever an activation function is called for which a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure is not specified.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0b36c-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="0b36c-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a><span data-ttu-id="0b36c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b36c-107">Remarks</span></span>

<span data-ttu-id="0b36c-108">**RemoteServerName** permite la administración de la configuración sencilla de las aplicaciones cliente. se pueden escribir sin nombres de servidor codificados de forma rígida y se pueden configurar modificando los valores del registro **RemoteServerName** de las clases de objetos que usan.</span><span class="sxs-lookup"><span data-stu-id="0b36c-108">**RemoteServerName** allows simple configuration management of client applications; they may be written without hard-coded server names and can be configured by modifying the **RemoteServerName** registry values of the classes of objects they use.</span></span>

<span data-ttu-id="0b36c-109">Como se describe en la documentación de la enumeración [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) y la estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , uno de los parámetros de la activación com distribuida es un puntero a una estructura **COSERVERINFO** .</span><span class="sxs-lookup"><span data-stu-id="0b36c-109">As described in the documentation for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration and the [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, one of the parameters of the distributed COM activation is a pointer to a **COSERVERINFO** structure.</span></span> <span data-ttu-id="0b36c-110">Cuando este valor no es **null**, la información de la estructura **COSERVERINFO** invalida el valor de la clave **RemoteServerName** para la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="0b36c-110">When this value is not **NULL**, the information in the **COSERVERINFO** structure overrides the setting of the **RemoteServerName** key for the function call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b36c-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0b36c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b36c-112">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="0b36c-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 
---
title: Clave de interfaz
description: Registra nuevas interfaces asociando un nombre de interfaz a un identificador de interfaz (IID). Debe haber una subclave IID para cada nueva interfaz.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Interfaz de la clave del registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076081"
---
# <a name="interface-key"></a><span data-ttu-id="ab526-105">Clave de interfaz</span><span class="sxs-lookup"><span data-stu-id="ab526-105">Interface Key</span></span>

<span data-ttu-id="ab526-106">Registra nuevas interfaces asociando un nombre de interfaz a un identificador de interfaz (IID).</span><span class="sxs-lookup"><span data-stu-id="ab526-106">Registers new interfaces by associating an interface name with an interface ID (IID).</span></span> <span data-ttu-id="ab526-107">Debe haber una subclave IID para cada nueva interfaz.</span><span class="sxs-lookup"><span data-stu-id="ab526-107">There must be one IID subkey for each new interface.</span></span>

## <a name="registry-key"></a><span data-ttu-id="ab526-108">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="ab526-108">Registry Key</span></span>

<span data-ttu-id="ab526-109">**HKEY \_ \_Interfaz de \\ \\ clases de \\ software de máquina local** \\ *{* IID *}*</span><span class="sxs-lookup"><span data-stu-id="ab526-109">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Interface**\\ *{* IID *}*</span></span>



| <span data-ttu-id="ab526-110">Valor del Registro</span><span class="sxs-lookup"><span data-stu-id="ab526-110">Registry value</span></span>                               | <span data-ttu-id="ab526-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab526-111">Description</span></span>                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab526-112">**BaseInterface**</span><span class="sxs-lookup"><span data-stu-id="ab526-112">**BaseInterface**</span></span>](baseinterface.md)       | <span data-ttu-id="ab526-113">Identifica la interfaz de la que se deriva la interfaz actual.</span><span class="sxs-lookup"><span data-stu-id="ab526-113">Identifies the interface from which the current interface is derived.</span></span>                                  |
| [<span data-ttu-id="ab526-114">**NumMethods**</span><span class="sxs-lookup"><span data-stu-id="ab526-114">**NumMethods**</span></span>](nummethods.md)             | <span data-ttu-id="ab526-115">Contiene el número de métodos de la interfaz asociada, incluidos los métodos de las interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="ab526-115">Contains the number of methods in the associated interface, including methods from derived interfaces.</span></span> |
| [<span data-ttu-id="ab526-116">**ProxyStubClsid**</span><span class="sxs-lookup"><span data-stu-id="ab526-116">**ProxyStubClsid**</span></span>](proxystubclsid.md)     | <span data-ttu-id="ab526-117">Asigna un IID a un CLSID en archivos dll de proxy de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ab526-117">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>                                                           |
| [<span data-ttu-id="ab526-118">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="ab526-118">**ProxyStubClsid32**</span></span>](proxystubclsid32.md) | <span data-ttu-id="ab526-119">Asigna un IID a un CLSID en dll de proxy de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ab526-119">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="ab526-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab526-120">Remarks</span></span>

<span data-ttu-id="ab526-121">La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.</span><span class="sxs-lookup"><span data-stu-id="ab526-121">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab526-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab526-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab526-123">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="ab526-123">**Interface**</span></span>](interface.md)
</dt> </dl>

 

 





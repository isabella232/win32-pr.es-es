---
title: Tratar
description: Especifica el CLSID de una clase que puede emular la clase actual.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- Clave del registro treatAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903601"
---
# <a name="treatas"></a><span data-ttu-id="0e35a-104">Tratar</span><span class="sxs-lookup"><span data-stu-id="0e35a-104">TreatAs</span></span>

<span data-ttu-id="0e35a-105">Especifica el CLSID de una clase que puede emular la clase actual.</span><span class="sxs-lookup"><span data-stu-id="0e35a-105">Specifies the CLSID of a class that can emulate the current class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0e35a-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="0e35a-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a><span data-ttu-id="0e35a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e35a-107">Remarks</span></span>

<span data-ttu-id="0e35a-108">Este es un valor de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="0e35a-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="0e35a-109">La emulación es la capacidad de una aplicación para abrir y editar un objeto de una clase diferente, a la vez que conserva el formato original del objeto.</span><span class="sxs-lookup"><span data-stu-id="0e35a-109">Emulation is the ability of one application to open and edit an object of a different class, while retaining the original format of the object.</span></span> <span data-ttu-id="0e35a-110">La resolución se produce en el equipo local, por lo que en el caso de la activación remota, la resolución se produce en el equipo cliente mediante el CLSID especificado por **treatAs**.</span><span class="sxs-lookup"><span data-stu-id="0e35a-110">Resolution occurs on the local computer, so in remote activation case, resolution occurs on the client computer using the CLSID specified by **TreatAs**.</span></span>

<span data-ttu-id="0e35a-111">DCOM busca en el registro local los **tratados**, aunque llame a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) y especifique un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="0e35a-111">DCOM looks at the local registry for **TreatAs**, even if you call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function and specify a remote server.</span></span> <span data-ttu-id="0e35a-112">Esto significa que si tiene una entrada **treatAs** para que Class1 se trate como clase2 en el equipo local, pero llama a **CoCreateInstance** para crear una instancia de Class1 y especifica un servidor remoto, DCOM intentará crear una instancia de clase2 en el servidor remoto, incluso si clase2 no está registrado en el servidor remoto, lo que hará que se produzca un error en la llamada a **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="0e35a-112">This means that if you have a **TreatAs** entry for Class1 to be treated as Class2 on your local computer, but you call **CoCreateInstance** to create an instance of Class1 and you specify a remote server, DCOM will try to create an instance of Class2 on the remote server, even if Class2 is not registered on the remote server, which will cause the call to **CoCreateInstance** to fail.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e35a-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e35a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e35a-114">**Autotreatas**</span><span class="sxs-lookup"><span data-stu-id="0e35a-114">**AutoTreatAs**</span></span>](autotreatas.md)
</dt> <dt>

[<span data-ttu-id="0e35a-115">**CoGetTreatAsClass**</span><span class="sxs-lookup"><span data-stu-id="0e35a-115">**CoGetTreatAsClass**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[<span data-ttu-id="0e35a-116">**CoTreatAsClass**</span><span class="sxs-lookup"><span data-stu-id="0e35a-116">**CoTreatAsClass**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 





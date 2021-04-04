---
title: Clave FileType
description: Usado por GetClassFile para comparar patrones con distintos bytes de archivo en un archivo no compuesto.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Clave del registro FileType COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076288"
---
# <a name="filetype-key"></a><span data-ttu-id="b7c6b-104">Clave FileType</span><span class="sxs-lookup"><span data-stu-id="b7c6b-104">FileType Key</span></span>

<span data-ttu-id="b7c6b-105">Usado por [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) para comparar patrones con distintos bytes de archivo en un archivo no compuesto.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-105">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b7c6b-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="b7c6b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span data-ttu-id="b7c6b-107"><span id="offset"></span><span id="OFFSET"></span>*posición*</span><span class="sxs-lookup"><span data-stu-id="b7c6b-107"><span id="offset"></span><span id="OFFSET"></span>*offset*</span></span>
</dt> <dd>

<span data-ttu-id="b7c6b-108">Determina la distancia desde el principio o el final del archivo hasta que comienza la comparación.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-108">Determines how far from the beginning or end of the file to begin the comparison.</span></span> <span data-ttu-id="b7c6b-109">Si el desplazamiento es un valor negativo, la comparación comienza desde el final del archivo menos el valor de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-109">If the offset is a negative value, the comparison begins from the end of the file minus the offset value.</span></span> <span data-ttu-id="b7c6b-110">El valor de desplazamiento es un tipo decimal a menos que vaya precedido de "0x".</span><span class="sxs-lookup"><span data-stu-id="b7c6b-110">The offset value is a decimal type unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="b7c6b-111"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="b7c6b-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="b7c6b-112">Representa la longitud en bytes desde el principio hasta el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-112">Represents the length in bytes from the beginning to the end of the file.</span></span> <span data-ttu-id="b7c6b-113">Representa el intervalo de bytes del archivo.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-113">Represents the byte range in the file.</span></span> <span data-ttu-id="b7c6b-114">El valor *CB* es un decimal a menos que esté precedido de "0x".</span><span class="sxs-lookup"><span data-stu-id="b7c6b-114">The *cb* value is a decimal unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="b7c6b-115"><span id="mask"></span><span id="MASK"></span>*máscara*</span><span class="sxs-lookup"><span data-stu-id="b7c6b-115"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="b7c6b-116">Valor binario utilizado para enmascaramiento, que se realiza mediante una operación AND lógica y el intervalo de bytes especificado por *offset* y *CB*.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-116">A binary value used for masking, which is performed by using a logical AND operation, and the byte range specified by *offset* and *cb*.</span></span> <span data-ttu-id="b7c6b-117">Si se omite este valor, los bytes se establecen en todos.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-117">If this value is omitted, the bytes are set to all ones.</span></span> <span data-ttu-id="b7c6b-118">Este valor siempre es hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-118">This value is always hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="b7c6b-119"><span id="value"></span><span id="VALUE"></span>*valor*</span><span class="sxs-lookup"><span data-stu-id="b7c6b-119"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="b7c6b-120">Representa el patrón que debe coincidir para que un archivo sea de este tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-120">Represents the pattern that must match for a file to be of this file type.</span></span> <span data-ttu-id="b7c6b-121">El patrón se usa para identificar correctamente un formato de archivo conocido de su contenido, no de su extensión.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-121">The pattern is used to properly identify a known file format from its contents, not by its extension.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7c6b-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7c6b-122">Remarks</span></span>

<span data-ttu-id="b7c6b-123">La función [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa las entradas para buscar coincidencias de patrones con distintos bytes de archivo en un archivo no compuesto.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-123">Entries are used by the [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) function to match patterns against various file bytes in a non-compound file.</span></span> <span data-ttu-id="b7c6b-124">**Filetype** tiene subclaves CLSID, cada una de las cuales tiene una serie de subclaves **0**, **1**, **2**, **3**.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-124">**FileType** has CLSID subkeys, each of which has a series of subkeys **0**, **1**, **2**, **3**.</span></span> <span data-ttu-id="b7c6b-125">Estos valores contienen patrones que, si coinciden, producen el CLSID indicado.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-125">These values contain patterns that, if one matches, yield the indicated CLSID.</span></span> <span data-ttu-id="b7c6b-126">Por ejemplo, un valor de "0, 4, FFFFFFFF, ABCD1234" indica que los cuatro primeros bytes deben ser ABCD1234, en ese orden.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-126">For example, a value of "0, 4, FFFFFFFF, ABCD1234" indicates that the first 4 bytes must be ABCD1234, in that order.</span></span> <span data-ttu-id="b7c6b-127">Un valor de "-4, 4, FEFEFEFE" indica que los últimos cuatro bytes del archivo deben ser FEFEFEFE.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-127">A value of "-4, 4, FEFEFEFE " indicates that the last four bytes in the file must be FEFEFEFE.</span></span> <span data-ttu-id="b7c6b-128">Si cualquiera de los patrones coincide, se devuelve el CLSID.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-128">If either pattern matches, the CLSID is returned.</span></span>

<span data-ttu-id="b7c6b-129">La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.</span><span class="sxs-lookup"><span data-stu-id="b7c6b-129">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7c6b-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7c6b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7c6b-131">**<extensión de archivo \_>**</span><span class="sxs-lookup"><span data-stu-id="b7c6b-131">**<file\_extension>**</span></span>](-file-extension--key.md)
</dt> <dt>

[<span data-ttu-id="b7c6b-132">**GetClassFile**</span><span class="sxs-lookup"><span data-stu-id="b7c6b-132">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 





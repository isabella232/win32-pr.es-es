---
description: Representa información sobre un archivo de código fuente.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SourceFileInfo (estructura)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b6afd5f3b383aff5c6d5168b259b13fe4429ac40d5b19a21c8e2f6a207cecd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119239"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo (estructura)

Representa información sobre un archivo de código fuente.

## <a name="syntax"></a>Sintaxis


```C++
} SourceFileInfo;
```

## <a name="members"></a>Miembros

**fileName**  
Cadena COM que contiene la ruta de archivo del archivo de origen asociado.

**checksumByteCount**  
Número de bytes de la suma de comprobación. Cuando checkSumAlgorithm es igual a CHECKSUMALGORITHM::md5, checkSumByteCount es 16. Cuando checkSumAlgorithm es igual a CHECKSUMALGORITHM::sha1, checkSumByteCount es 20.

**checkSumAlgorithm**  
Especifica el algoritmo utilizado para generar la suma de comprobación del archivo. Los algoritmos admitidos son MD5 y SHA1. Para obtener más información, vea la enumeración CHECKSUMALGORITHM.

**checkSumFirstPart**  
Primera parte de 8 bytes de la suma de comprobación.

**checkSumSecondPart**  
Segunda parte de 8 bytes de la suma de comprobación.

**checkSumThirdPart**  
Tercera parte de 8 bytes de la suma de comprobación.

**checkSumFourthPart**  
Cuarta parte de 8 bytes de la suma de comprobación.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 




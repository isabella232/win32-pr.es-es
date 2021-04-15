---
description: Representa información sobre un archivo de código fuente.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura SourceFileInfo
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
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495245"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span id="vspixengine.sourcefileinfo"></span>Estructura SourceFileInfo

Representa información sobre un archivo de código fuente.

## <a name="syntax"></a>Sintaxis


```C++
} SourceFileInfo;
```

## <a name="members"></a>Miembros

**fileName**  
Una cadena COM comtaining la ruta de acceso del archivo de código fuente asociado.

**checksumByteCount**  
Número de bytes de la suma de comprobación. Cuando checkSumAlgorithm es igual a CHECKSUMALGORITHM:: MD5, checkSumByteCount es 16. Cuando checkSumAlgorithm es igual a CHECKSUMALGORITHM:: SHA1, checkSumByteCount es 20.

**checkSumAlgorithm**  
Especifica el algoritmo utilizado para generar la suma de comprobación del archivo. Los algoritmos admitidos son MD5 y SHA1. Para obtener más información, consulte la enumeración CHECKSUMALGORITHM.

**checkSumFirstPart**  
La primera parte de 8 bytes de la suma de comprobación.

**checkSumSecondPart**  
La segunda parte de 8 bytes de la suma de comprobación.

**checkSumThirdPart**  
La tercera parte de 8 bytes de la suma de comprobación.

**checkSumFourthPart**  
Cuarta parte de 8 bytes de la suma de comprobación.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 




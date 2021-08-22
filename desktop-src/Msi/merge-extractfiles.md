---
description: El método ExtractFiles del objeto Merge extrae el archivo .cab incrustado de un módulo y, a continuación, escribe esos archivos en el directorio de destino.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Método Merge.ExtractFiles (Advpub.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e56d6572526e2aecfc12dc5b2bb9a365be6d3c53b6fb1707fe197c056d05c377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926565"
---
# <a name="mergeextractfiles-method"></a>Método Merge.ExtractFiles

El **método ExtractFiles** del objeto [**Merge**](merge-object.md) extrae el archivo .cab incrustado de un módulo y, a continuación, escribe esos archivos en el directorio de destino.

## <a name="syntax"></a>Sintaxis


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ruta de acceso* 
</dt> <dd>

Directorio de destino completo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se sobrescriben los archivos del directorio de destino con el mismo nombre. La ruta de acceso se crea si aún no existe.

**ExtractFiles siempre** extrae archivos mediante nombres de archivo cortos para la ruta de acceso. Para usar nombres de archivo largos para la ruta de acceso, use el [**método ExtractFilesEx**](merge-extractfilesex.md).

### <a name="c"></a>C++

Vea [**Función ExtractFiles.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                                     |
| Header<br/>  | <dl> <dt>Advpub.h (incluya Mergemod.h)</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 

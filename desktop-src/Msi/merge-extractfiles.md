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
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071902"
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

*Path* 
</dt> <dd>

Directorio de destino completo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se sobrescriben los archivos del directorio de destino con el mismo nombre. La ruta de acceso se crea si aún no existe.

**ExtractFiles** siempre extrae archivos mediante nombres de archivo cortos para la ruta de acceso. Para usar nombres de archivo largos para la ruta de acceso, use el [**método ExtractFilesEx**](merge-extractfilesex.md).

### <a name="c"></a>C++

Vea [**Función ExtractFiles.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                                     |
| Encabezado<br/>  | <dl> <dt>Advpub.h (incluir Mergemod.h)</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 

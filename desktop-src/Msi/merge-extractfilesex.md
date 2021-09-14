---
description: El método ExtractFilesEx del objeto Merge extrae el archivo .cab incrustado de un módulo y, a continuación, escribe esos archivos en el directorio de destino.
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: Método Merge.ExtractFilesEx (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074387"
---
# <a name="mergeextractfilesex-method"></a>Método Merge.ExtractFilesEx

El **método ExtractFilesEx** del objeto [**Merge**](merge-object.md) extrae el archivo .cab incrustado de un módulo y, a continuación, escribe esos archivos en el directorio de destino.

## <a name="syntax"></a>Sintaxis


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Path* 
</dt> <dd>

Directorio de destino completo.

</dd> <dt>

*fLongFileNames* 
</dt> <dd>

Se establece para especificar el uso de nombres de archivo largos para segmentos de ruta de acceso y nombres de archivo finales.

</dd> <dt>

*pFilePaths* 
</dt> <dd>

Se trata de una lista de rutas de acceso completas para los archivos que se extrajeron correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se sobrescriben los archivos del directorio de destino con el mismo nombre. La ruta de acceso se crea si aún no existe.

### <a name="c"></a>C++

Vea [**Función ExtractFilesEx.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 





---
description: El método ExtractFiles del objeto Merge extrae el archivo. cab incrustado de un módulo y, a continuación, escribe esos archivos en el directorio de destino.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Merge. ExtractFiles (método) (Advpub. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670800"
---
# <a name="mergeextractfiles-method"></a>Merge. ExtractFiles (método)

El método **ExtractFiles** del objeto [**Merge**](merge-object.md) extrae el archivo. cab incrustado de un módulo y, a continuación, escribe esos archivos en el directorio de destino.

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

## <a name="remarks"></a>Observaciones

Se sobrescriben los archivos del directorio de destino con el mismo nombre. Si aún no existe, se crea la ruta de acceso.

**ExtractFiles** siempre extrae los archivos con nombres de archivo cortos para la ruta de acceso. Para utilizar nombres de archivo largos para la ruta de acceso, use el [**método ExtractFilesEx**](merge-extractfilesex.md).

### <a name="c"></a>C++

Vea [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) (función).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                                     |
| Encabezado<br/>  | <dl> <dt>Advpub. h (incluye Mergemod. h)</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 

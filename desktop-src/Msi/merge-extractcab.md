---
description: El método ExtractCAB del objeto Merge extrae el archivo. cab incrustado de un módulo y lo guarda como el archivo especificado. El instalador crea este archivo si aún no existe y se sobrescribe si existe.
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: Método Merge. ExtractCAB (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670452"
---
# <a name="mergeextractcab-method"></a>Merge. ExtractCAB (método)

El método **ExtractCAB** del objeto [**Merge**](merge-object.md) extrae el archivo. cab incrustado de un módulo y lo guarda como el archivo especificado. El instalador crea este archivo si aún no existe y se sobrescribe si existe.

## <a name="syntax"></a>Sintaxis


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileName* 
</dt> <dd>

El archivo de destino completo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="c"></a>C++

Consulte función [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 

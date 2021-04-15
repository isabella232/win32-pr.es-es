---
description: El método OpenLog del objeto Merge abre un archivo de registro que recibe los mensajes de progreso y de error. Si el archivo de registro ya existe, el instalador anexa los nuevos mensajes. Si el archivo de registro no existe, el instalador crea un archivo de registro.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Método Merge. OpenLog (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654023"
---
# <a name="mergeopenlog-method"></a>Merge. OpenLog (método)

El método **openlog** del objeto [**Merge**](merge-object.md) abre un archivo de registro que recibe los mensajes de progreso y de error. Si el archivo de registro ya existe, el instalador anexa los nuevos mensajes. Si el archivo de registro no existe, el instalador crea un archivo de registro.

## <a name="syntax"></a>Sintaxis


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de archivo* 
</dt> <dd>

Nombre de archivo completo que apunta a un archivo para abrirlo o crearlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los clientes pueden enviar sus propios mensajes a este archivo de registro a través del método [**log**](merge-log.md) .

### <a name="c"></a>C++

Consulte función [**openlog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 

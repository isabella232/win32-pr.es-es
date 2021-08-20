---
description: El método OpenLog del objeto Merge abre un archivo de registro que recibe mensajes de progreso y error. Si el archivo de registro ya existe, el instalador anexa nuevos mensajes. Si el archivo de registro no existe, el instalador crea un archivo de registro.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Método Merge.OpenLog (Mergemod.h)
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
ms.openlocfilehash: c69ecf0c7a4a629b2f6ebc303d34619ae9d4cc396c79e09ea37e2d4b27db5c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804617"
---
# <a name="mergeopenlog-method"></a>Método Merge.OpenLog

El **método OpenLog** del objeto [**Merge**](merge-object.md) abre un archivo de registro que recibe mensajes de progreso y error. Si el archivo de registro ya existe, el instalador anexa nuevos mensajes. Si el archivo de registro no existe, el instalador crea un archivo de registro.

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

Nombre de archivo completo que apunta a un archivo que se debe abrir o crear.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Los clientes pueden enviar sus propios mensajes a este archivo de registro a través del [**método Log.**](merge-log.md)

### <a name="c"></a>C++

Consulte [**Función OpenLog.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 

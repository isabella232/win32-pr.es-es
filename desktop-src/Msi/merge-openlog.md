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
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473978"
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

## <a name="remarks"></a>Observaciones

Los clientes pueden enviar sus propios mensajes a este archivo de registro a través del [**método Log.**](merge-log.md)

### <a name="c"></a>C++

Consulte [**Función OpenLog.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 

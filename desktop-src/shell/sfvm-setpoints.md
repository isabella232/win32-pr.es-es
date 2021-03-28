---
description: Establece los puntos de los objetos seleccionados actualmente en el objeto de datos en los comandos de copiar y cortar. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_SETPOINTS (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279389"
---
# <a name="sfvm_setpoints-message"></a>SFVM \_ SETPOINTS

Establece los puntos de los objetos seleccionados actualmente en el objeto de datos en los comandos de **copiar** y **cortar** . Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdtobj* \[ de\]
</dt> <dd>Un puntero a un <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> de los comandos de **copiar** y **cortar** .</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve cero.

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 

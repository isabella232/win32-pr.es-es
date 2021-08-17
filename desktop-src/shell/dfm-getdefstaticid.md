---
description: Enviado por la implementación predeterminada del menú contextual durante la creación, especificando el comando de menú predeterminado y permitiendo una opción alternativa. Usado por LPFNDFMCALLBACK.
title: DFM_GETDEFSTATICID mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4d987e085779fd58f16c2534b517c39ebb4b7e3c6e2829982881015bb3a59a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094376"
---
# <a name="dfm_getdefstaticid-message"></a>Mensaje \_ GETDEFSTATICID de DFM

Enviado por la implementación predeterminada del menú contextual durante la creación, especificando el comando de menú predeterminado y permitiendo una opción alternativa. Usado por [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*defaultID* \[ in, out\]
</dt> <dd>

Puntero al identificador del comando de menú seleccionado. Se reconoce la marca siguiente.

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**PROPIEDADES DE CMD DE DFM \_ \_**


</dt> <dd>

Mostrar la **interfaz de** usuario propiedades del elemento en el que se invocó el menú.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Para invalidar la opción de comando predeterminada, el controlador debe, tras recibir este mensaje, establecer el valor al que apunta *defaultID* en el identificador del comando de reemplazo y devolver S \_ OK. Devuelve un código de error de lo contrario.

Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada en función de cómo se construya el objeto de menú contextual predeterminado. Hay dos API para su construcción, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)y [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX es**](dfm-invokecommandex.md) una versión extendida de este mensaje y proporciona más información a la devolución de llamada. Use **DFM \_ INVOKECOMMANDEX si** la información adicional proporcionada por esa interfaz es necesaria en la implementación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 

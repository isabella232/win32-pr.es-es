---
description: Se envía a un archivo DLL de extensión cuando el administrador de archivos está cargando el archivo DLL.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: Mensaje de FMEVENT_LOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985514"
---
# <a name="fmevent_load-message"></a>Mensaje de carga de FMEVENT \_

Se envía a un archivo DLL de extensión cuando el administrador de archivos está cargando el archivo DLL.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lpfmsld* 
</dt> <dd>

La dirección de una estructura de [**\_ carga de FMS**](fms-load.md) que especifica el valor Delta del elemento de menú.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un archivo DLL de extensión debe devolver **true** para continuar cargando el archivo dll. Si el archivo DLL devuelve **false**, el administrador de archivos llama a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) y finaliza cualquier comunicación con el archivo dll de extensión.

## <a name="remarks"></a>Observaciones

Una aplicación debe rellenar los miembros **dwSize**, **szMenuName** y **hMenu** en la estructura de [**\_ carga de FMS**](fms-load.md) . También debe guardar el valor del miembro **wMenuDelta** y usarlo para identificar los elementos de menú al modificar el menú.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 

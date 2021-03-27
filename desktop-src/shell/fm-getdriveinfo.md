---
description: Enviado por una extensión del administrador de archivos para recuperar la información de la unidad de la ventana del administrador de archivos activo.
title: Mensaje de FM_GETDRIVEINFO (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997220"
---
# <a name="fm_getdriveinfo-message"></a>\_Mensaje GETDRIVEINFO de FM

Enviado por una extensión del administrador de archivos para recuperar la información de la unidad de la ventana del administrador de archivos activo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lpfmsgdi* 
</dt> <dd>

La dirección de una estructura de [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) que recibe información de la unidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero.

## <a name="remarks"></a>Observaciones

Si se devuelve 0xFFFFFFFF en el miembro **dwTotalSpace** o **dwFreeSpace** de la estructura de [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) , la biblioteca de extensiones debe calcular el valor o los valores.

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

 

 





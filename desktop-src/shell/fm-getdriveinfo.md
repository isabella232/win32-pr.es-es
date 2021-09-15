---
description: Enviado por una extensión del Administrador de archivos para recuperar información de unidad desde la ventana activa del Administrador de archivos.
title: FM_GETDRIVEINFO mensaje (Wfext.h)
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
ms.openlocfilehash: 0abac794ed23eca30676a839a6eb5ad7c1079c3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579597"
---
# <a name="fm_getdriveinfo-message"></a>Mensaje \_ GETDRIVEINFO de FM

Enviado por una extensión del Administrador de archivos para recuperar información de unidad desde la ventana activa del Administrador de archivos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lpfmsgdi* 
</dt> <dd>

Dirección de una estructura [**\_ GETDRIVEINFO de FMS**](fms-getdriveinfo.md) que recibe información de unidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve distinto de cero.

## <a name="remarks"></a>Observaciones

Si 0xFFFFFFFF en el **miembro dwTotalSpace** o **dwFreeSpace** de la estructura [**\_ GETDRIVEINFO de FMS,**](fms-getdriveinfo.md) la biblioteca de extensiones debe calcular el valor o los valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 





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
ms.openlocfilehash: 39df15a4522e863fada40d3c964d709f40d2a26d01240aaefe51b09924b8c9ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459125"
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

Devuelve un valor distinto de cero.

## <a name="remarks"></a>Comentarios

Si 0xFFFFFFFF en el **miembro dwTotalSpace** o **dwFreeSpace** de la estructura [**\_ GETDRIVEINFO de FMS,**](fms-getdriveinfo.md) la biblioteca de extensiones debe calcular el valor o los valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 





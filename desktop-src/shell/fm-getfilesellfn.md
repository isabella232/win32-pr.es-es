---
description: Enviado por una extensión del Administrador de archivos para recuperar información sobre un archivo seleccionado desde la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda). El archivo seleccionado puede tener un nombre de archivo largo.
title: FM_GETFILESELLFN mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: 2074fb1e631edf1795b8f0d15ea9f0d40e90556d527899873ef88195c2367576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860772"
---
# <a name="fm_getfilesellfn-message"></a>Mensaje \_ GETFILESELLFN de FM

Enviado por una extensión del Administrador de archivos para recuperar información sobre un archivo seleccionado desde la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda). El archivo seleccionado puede tener un nombre de archivo largo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*índice* 
</dt> <dd>

Índice de base cero del archivo seleccionado que se recuperará.

</dd> <dt>

*lpfmsgfs* 
</dt> <dd>

Dirección de una [**estructura \_ GETFILESEL de FMS**](fms-getfilesel.md) que recibe información sobre la selección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero del archivo seleccionado que se recuperó.

## <a name="remarks"></a>Comentarios

Solo las extensiones que admiten nombres de archivo largos (por ejemplo, extensiones compatibles con la red) deben usar este mensaje.

Una extensión puede usar el [**mensaje \_ FM GETSELCOUNTLFN**](fm-getselcountlfn.md) para recuperar el recuento de archivos seleccionados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FM \_ GETFILESEL**](fm-getfilesel.md)
</dt> <dt>

[**FM \_ GETSELCOUNT**](fm-getselcount.md)
</dt> </dl>

 

 





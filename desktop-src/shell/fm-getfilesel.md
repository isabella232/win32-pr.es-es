---
description: Enviado por una extensión del administrador de archivos para recuperar información sobre un archivo seleccionado en la ventana del administrador de archivos activo (la ventana de directorio o la ventana de resultados de la búsqueda).
title: Mensaje de FM_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: ec7d221e0c352c4b9284ae5fe2d6f80e50da85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909565"
---
# <a name="fm_getfilesel-message"></a>\_Mensaje GETFILESEL de FM

Enviado por una extensión del administrador de archivos para recuperar información sobre un archivo seleccionado en la ventana del administrador de archivos activo (la ventana de directorio o la ventana de resultados de la búsqueda).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*índice* 
</dt> <dd>

Índice de base cero del archivo seleccionado que se va a recuperar.

</dd> <dt>

*lpfmsgfs* 
</dt> <dd>

Dirección de una estructura de [**FMS \_ GETFILESEL**](fms-getfilesel.md) que recibe información sobre la selección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero del archivo seleccionado que se ha recuperado.

## <a name="remarks"></a>Observaciones

Una extensión puede usar el [**mensaje \_ GETSELCOUNT de FM**](fm-getselcount.md) para recuperar el recuento de archivos seleccionados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**\_GETFILESELLFN FM**](fm-getfilesellfn.md)
</dt> <dt>

[**\_GETSELCOUNTLFN FM**](fm-getselcountlfn.md)
</dt> </dl>

 

 





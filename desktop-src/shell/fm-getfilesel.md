---
description: Enviado por una extensión del Administrador de archivos para recuperar información sobre un archivo seleccionado desde la ventana activa del Administrador de archivos (ya sea la ventana de directorio o la ventana Resultados de la búsqueda).
title: FM_GETFILESEL mensaje (Wfext.h)
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
ms.openlocfilehash: 2da95a39f8e84215640e926ae21a043865223665
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841426"
---
# <a name="fm_getfilesel-message"></a>Mensaje \_ GETFILESEL de FM

Enviado por una extensión del Administrador de archivos para recuperar información sobre un archivo seleccionado desde la ventana activa del Administrador de archivos (ya sea la ventana de directorio o la ventana Resultados de la búsqueda).

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

## <a name="remarks"></a>Observaciones

Una extensión puede usar el [**mensaje \_ GETSELCOUNT de FM**](fm-getselcount.md) para recuperar el recuento de archivos seleccionados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FM \_ GETFILESELLFN**](fm-getfilesellfn.md)
</dt> <dt>

[**FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md)
</dt> </dl>

 

 





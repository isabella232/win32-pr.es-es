---
description: Enviado por una extensión del administrador de archivos para recuperar información sobre un archivo seleccionado en la ventana del administrador de archivos activo (la ventana de directorio o la ventana de resultados de la búsqueda). El archivo seleccionado puede tener un nombre de archivo largo.
title: Mensaje de FM_GETFILESELLFN (Wfext. h)
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
ms.openlocfilehash: 847100f494772b3c59ad719d03d7bc2dbe28cc29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496787"
---
# <a name="fm_getfilesellfn-message"></a>\_Mensaje GETFILESELLFN de FM

Enviado por una extensión del administrador de archivos para recuperar información sobre un archivo seleccionado en la ventana del administrador de archivos activo (la ventana de directorio o la ventana de resultados de la búsqueda). El archivo seleccionado puede tener un nombre de archivo largo.

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

Solo las extensiones que admiten nombres de archivo largos (por ejemplo, extensiones basadas en red) deben utilizar este mensaje.

Una extensión puede usar el [**mensaje \_ GETSELCOUNTLFN de FM**](fm-getselcountlfn.md) para recuperar el recuento de archivos seleccionados.

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

[**\_GETFILESEL FM**](fm-getfilesel.md)
</dt> <dt>

[**\_GETSELCOUNT FM**](fm-getselcount.md)
</dt> </dl>

 

 





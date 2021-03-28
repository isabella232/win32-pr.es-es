---
description: Enviado por una extensión del administrador de archivos para recuperar el tipo de ventana del administrador de archivos que tiene el foco de entrada.
title: Mensaje de FM_GETFOCUS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: af6e0894b3734f976302eacbf0575a017f054f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985527"
---
# <a name="fm_getfocus-message"></a>\_Mensaje GETFOCUS de FM

Enviado por una extensión del administrador de archivos para recuperar el tipo de ventana del administrador de archivos que tiene el foco de entrada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tipo de ventana del administrador de archivos que tiene el foco de entrada. Puede ser uno de los siguientes valores.



| Código devuelto                                                                                    | Descripción                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**FMFOCUS \_ dir**</dt> </dl>    | Parte del directorio de una ventana de directorio.<br/> |
| <dl> <dt>**\_árbol FMFOCUS**</dt> </dl>   | Parte de árbol de una ventana de directorio.<br/>      |
| <dl> <dt>**\_unidades FMFOCUS**</dt> </dl> | Barra de unidad de una ventana de directorio.<br/>         |
| <dl> <dt>**búsqueda de FMFOCUS \_**</dt> </dl> | Ventana Resultados de la búsqueda.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



 

 





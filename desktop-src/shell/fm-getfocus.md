---
description: Enviado por una extensión del Administrador de archivos para recuperar el tipo de ventana del Administrador de archivos que tiene el foco de entrada.
title: FM_GETFOCUS mensaje (Wfext.h)
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
ms.openlocfilehash: 7512595008ad79d33bf1ac9b381b63831977282b83a8ce595c3d2689087c869c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459115"
---
# <a name="fm_getfocus-message"></a>Mensaje \_ GETFOCUS de FM

Enviado por una extensión del Administrador de archivos para recuperar el tipo de ventana del Administrador de archivos que tiene el foco de entrada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tipo de ventana del Administrador de archivos que tiene el foco de entrada. Puede ser uno de los siguientes valores.



| Código devuelto                                                                                    | Descripción                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**FMFOCUS \_ DIR**</dt> </dl>    | Parte del directorio de una ventana de directorio.<br/> |
| <dl> <dt>**ÁRBOL \_ FMFOCUS**</dt> </dl>   | Parte del árbol de una ventana de directorio.<br/>      |
| <dl> <dt>**UNIDADES FMFOCUS \_**</dt> </dl> | Barra de unidad de una ventana de directorio.<br/>         |
| <dl> <dt>**FMFOCUS \_ SEARCH**</dt> </dl> | Ventana Resultados de la búsqueda.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



 

 





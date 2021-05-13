---
description: Se envía a un archivo DLL de extensión cuando el usuario selecciona un nombre de archivo en la ventana de directorio del Administrador de archivos o en la ventana Resultados de la búsqueda.
title: FMEVENT_SELCHANGE mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: e9aa647434aab5a483626757179a7b23b3372a02
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842266"
---
# <a name="fmevent_selchange-message"></a>Mensaje \_ FMEVENT SELCHANGE

Se envía a un archivo DLL de extensión cuando el usuario selecciona un nombre de archivo en la ventana de directorio del Administrador de archivos o en la ventana Resultados de la búsqueda.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un archivo DLL de extensión debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Los cambios en la parte del árbol de la ventana de directorio no generan este mensaje.

Dado que el usuario puede cambiar la selección muchas veces, el archivo DLL de extensión debe devolver rápidamente después de procesar este mensaje para evitar ralentizar el proceso de selección del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 





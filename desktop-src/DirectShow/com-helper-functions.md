---
description: Estas funciones proporcionan compatibilidad para implementar la interfaz IUnknown en DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Funciones auxiliares de COM (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681187"
---
# <a name="com-helper-functions"></a>Funciones auxiliares de COM

Estas funciones proporcionan compatibilidad para implementar la interfaz **IUnknown** en DirectShow.



| Función                                               | Descripción                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [**DECLARAR \_ IUNKNOWN**](declare-iunknown.md)          | Declara los tres métodos de la interfaz base para una nueva interfaz. |
| [**GetInterface**](getinterface.md)                   | Recupera un puntero de interfaz al cliente solicitado.               |
| [**INonDelegatingUnknown**](inondelegatingunknown.md) | Versión no delegada de la interfaz **IUnknown** .                  |
| [**LoadOLEAut32**](loadoleaut32.md)                   | Carga el archivo DLL de automatización (OleAut32.dll).                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de la utilidad](utility-functions.md)
</dt> </dl>

 

 





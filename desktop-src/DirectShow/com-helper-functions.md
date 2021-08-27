---
description: Estas funciones proporcionan compatibilidad para implementar la interfaz IUnknown en DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Funciones auxiliares COM (Combase.h)
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
ms.openlocfilehash: fa8558cd0d04258adf89cbacdd99952cf00c6d0aa5f24ee38cca2dceb4e5478f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084345"
---
# <a name="com-helper-functions"></a>Funciones auxiliares COM

Estas funciones proporcionan compatibilidad para implementar la **interfaz IUnknown** en DirectShow.



| Función                                               | Descripción                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [**DECLARE \_ IUNKNOWN**](declare-iunknown.md)          | Declara los tres métodos de la interfaz base para una nueva interfaz. |
| [**GetInterface**](getinterface.md)                   | Recupera un puntero de interfaz al cliente solicitado.               |
| [**INonDelegatingUnknown**](inondelegatingunknown.md) | Versión no delegada de la **interfaz IUnknown.**                  |
| [**LoadOLEAut32**](loadoleaut32.md)                   | Carga el archivo DLL de Automation (OleAut32.dll).                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de la utilidad](utility-functions.md)
</dt> </dl>

 

 





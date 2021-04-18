---
description: Esta función finaliza forzosamente el programa de llamada si se invoca dentro de una llamada del cargador. De lo contrario, no tiene ningún efecto.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: LdrFastFailInLoaderCallout función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670416"
---
# <a name="ldrfastfailinloadercallout-function"></a>LdrFastFailInLoaderCallout función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Esta función finaliza forzosamente el programa de llamada si se invoca dentro de una llamada del cargador. De lo contrario, no tiene ningún efecto.

## <a name="syntax"></a>Sintaxis


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta rutina no detecta todos los posibles casos de interbloqueo; es posible que un subproceso dentro de una llamada del cargador adquiera un bloqueo mientras que un subproceso fuera de una llamada del cargador contiene el mismo bloqueo y realiza una llamada al cargador. En otras palabras, puede haber una inversión del orden de bloqueo entre el bloqueo del cargador y un bloqueo de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>NTDll. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>NTDll.dll</dt> </dl> |



 

 





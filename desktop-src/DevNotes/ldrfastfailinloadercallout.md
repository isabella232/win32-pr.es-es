---
description: Esta función finaliza de forma fuerza el programa que realiza la llamada si se invoca dentro de una llamada del cargador. De lo contrario, no tiene ningún efecto.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: Función LdrFastFailInLoaderCallout
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
ms.openlocfilehash: f944de64f26d814af799d1f8d2419c2dd9ade04970774e2581f446c0bd32c0fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001335"
---
# <a name="ldrfastfailinloadercallout-function"></a>Función LdrFastFailInLoaderCallout

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Esta función finaliza de forma fuerza el programa que realiza la llamada si se invoca dentro de una llamada del cargador. De lo contrario, no tiene ningún efecto.

## <a name="syntax"></a>Sintaxis


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta rutina no detecta todos los posibles casos de interbloqueo; Es posible que un subproceso dentro de una llamada de cargador adquiera un bloqueo mientras que algún subproceso fuera de una llamada del cargador contiene el mismo bloqueo y realiza una llamada al cargador. En otras palabras, puede haber una inversión de orden de bloqueo entre el bloqueo del cargador y un bloqueo de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>NTDll.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>NTDll.dll</dt> </dl> |



 

 





---
title: IConfigAsfWriter2 ResetMultiPassState, método
description: El método ResetMultiPassState restablece el filtro cuando se cancela un paso de codificación de preprocesamiento antes de que se complete.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Método ResetMultiPassState formato de Windows Media
- Método ResetMultiPassState formato de Windows Media, interfaz IConfigAsfWriter2
- Interfaz IConfigAsfWriter2 formato de Windows Media, método ResetMultiPassState
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421202"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a>IConfigAsfWriter2:: ResetMultiPassState (método)

El método **ResetMultiPassState** restablece el filtro cuando se cancela un paso de codificación de preprocesamiento antes de que se complete.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                         | Descripción                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                | El método se ha llevado a cabo de forma correcta.<br/>                  |
| <dl> <dt>**VFW \_ E \_ no \_ detenido**</dt> </dl> | El filtro no se encontraba en un estado detenido.<br/> |



 

## <a name="remarks"></a>Observaciones

Se debe llamar a este método para restablecer el estado interno del filtro siempre que se cancele un paso de codificación de preprocesamiento antes de que el filtro haya recibido un evento de **\_ \_ preprocesamiento de EC** . No es necesario llamar a este método si la fase de codificación de preprocesamiento se completa sin errores.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 


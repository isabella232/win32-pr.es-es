---
title: Método IConfigAsfWriter2 ResetMultiPassState
description: El método ResetMultiPassState restablece el filtro cuando se cancela un paso de codificación de preprocesamiento antes de que se complete.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Método ResetMultiPassState windows Media Format
- Método ResetMultiPassState windows Media Format , interfaz IConfigAsfWriter2
- IConfigAsfWriter2 interface windows Media Format , ResetMultiPassState method
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f10563ed716b6b33258fe57ff8129bff78b401170db1512566015d0b05d54dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839875"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a>IConfigAsfWriter2::ResetMultiPassState (método)

El **método ResetMultiPassState** restablece el filtro cuando se cancela un paso de codificación de preprocesamiento antes de que se complete.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                         | Descripción                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | El método se ha llevado a cabo de forma correcta.<br/>                  |
| <dl> <dt>**VFW \_ E \_ NOT \_ STOPPED**</dt> </dl> | El filtro no estaba en estado detenido.<br/> |



 

## <a name="remarks"></a>Comentarios

Se debe llamar a este método para restablecer el estado interno del filtro siempre que se cancele un paso de codificación de preprocesamiento antes de que el filtro haya recibido un evento **\_ EC PREPROCESS \_ COMPLETE.** No es necesario llamar a este método si el paso de codificación de preprocesamiento se completa sin errores.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConfigAsfWriter2 (Interfaz)**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 


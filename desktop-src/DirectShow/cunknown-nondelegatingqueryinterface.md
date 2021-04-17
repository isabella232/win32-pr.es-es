---
description: 'Recupera un puntero de interfaz e incrementa el recuento de referencias. Este método implementa el método INonDelegatingUnknown:: NonDelegatingQueryInterface.'
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Método CUnknown. NonDelegatingQueryInterface (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680877"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a>CUnknown. NonDelegatingQueryInterface, método

Recupera un puntero de interfaz e incrementa el recuento de referencias. Este método implementa el método **INonDelegatingUnknown:: NonDelegatingQueryInterface** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* 
</dt> <dd>

Identificador de la interfaz.

</dd> <dt>

*PPV* 
</dt> <dd>

Dirección de un puntero para recibir la interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                                |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | El objeto no admite esta interfaz.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Argumento de puntero **nulo** .<br/>              |



 

## <a name="remarks"></a>Observaciones

La clase **CUnknown** expone solo la interfaz **IUknown** . Invalide este método para exponer interfaces adicionales. Para obtener información sobre cómo invalidar este método, consulte [How to implement IUnknown](how-to-implement-iunknown.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 





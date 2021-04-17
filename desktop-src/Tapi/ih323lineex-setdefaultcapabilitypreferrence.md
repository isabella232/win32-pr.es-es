---
description: Configura las preferencias de las funciones predeterminadas.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'IH323LineEx:: SetDefaultCapabilityPreferrence (método) (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679231"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a>IH323LineEx:: SetDefaultCapabilityPreferrence (método)

\[**SetDefaultCapabilityPreferrence** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **SetDefaultCapabilityPreferrence** configura las preferencias de las funciones predeterminadas. Las capacidades tienen un peso predeterminado de 100. Si la aplicación especifica un mayor peso para una funcionalidad, tendrá una prioridad más alta durante la negociación H. 245. Si la aplicación establece el peso de una capacidad en 0, no se utilizará en la negociación H. 245.

Este método es acumulativo. Por ejemplo, si se llama primero a este método para deshabilitar una funcionalidad y se llama de nuevo para deshabilitar otra, ambas funciones se deshabilitarán como resultado de estas dos llamadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwNumCaps* \[ de\]
</dt> <dd>

Valor **DWORD** que contiene el número de funciones establecidas con este método.

</dd> <dt>

*pCapabilities* \[ de\]
</dt> <dd>

Una matriz de funcionalidades. Cada elemento de la matriz es un valor de [**\_ capacidad de H245**](h245-capability.md) .

</dd> <dt>

*pWeights* \[ de\]
</dt> <dd>

Matriz de pesos asociados a las funciones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                                                                                                                                                                                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pCapabilities* es **null**, el parámetro *pWeights* es **null**, o bien *pCapabilities* y *pWeights* son **null**, o bien la matriz pCapabilities contiene un objeto de funcionalidad H. 245 no válido.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>     | No se puede leer un elemento de la matriz *pWeights* o un elemento de la matriz *pCapabilities* .<br/>                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 





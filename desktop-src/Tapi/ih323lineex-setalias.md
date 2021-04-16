---
description: El método SetAlias configura un alias H. 323 predeterminado para la dirección. Este alias se usará en la llamada H. 323 configuración de Exchange para que la otra parte conozca el nombre de esta entidad.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: 'IH323LineEx:: SetAlias (método) (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690169"
---
# <a name="ih323lineexsetalias-method"></a>IH323LineEx:: SetAlias (método)

\[**SetAlias** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **SetAlias** configura un alias H. 323 predeterminado para la dirección. Este alias se usará en la llamada H. 323 configuración de Exchange para que la otra parte conozca el nombre de esta entidad.

Si se llama a este método por segunda vez, se sobrescribirá el alias anterior.

El alias establecido en esta interfaz solo se usará cuando no haya ninguna otra manera de que el TSP busque un alias adecuado. En el futuro, cuando se agrega la compatibilidad con Gatekeeper al TSP, el alias registrado en el equipo selector o asignado por el equipo selector invalidará lo que se establezca a través de este método.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strAlias* \[ de\]
</dt> <dd>

El alias que se va a usar, en Unicode. No es necesaria la terminación **nula** .

</dd> <dt>

*dwLength* \[ de\]
</dt> <dd>

La longitud del nombre de alias en número de caracteres, incluido el terminador **null** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                               | Descripción                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | El método se realizó correctamente.<br/>                                                                                                     |
| <dl> <dt>**\_puntero E**</dt> </dl> | El número de caracteres indicado en *dwLength* supera el número real de caracteres en el parámetro *strAlias* .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 





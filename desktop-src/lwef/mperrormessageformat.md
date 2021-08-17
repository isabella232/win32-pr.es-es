---
title: Función MpErrorMessageFormat (MpClient.h)
description: Devuelve un mensaje de error con formato basado en un código de error.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Función MpErrorMessageFormat Heredada de Windows environment
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 124bf9e2c5c2ecc18f286b99f0c3b93695abd3f6a40853fcc47de580edef5db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883512"
---
# <a name="mperrormessageformat-function"></a>Función MpErrorMessageFormat

Devuelve un mensaje de error con formato basado en un código de error.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMpHandle* \[ En\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*hrError* \[ En\]
</dt> <dd>

Tipo: **HRESULT**

Código de error basado en **HRESULT.**

</dd> <dt>

*pwszErrorDesc* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \***

Devuelve un mensaje de error con formato basado en *hrError*. Esta cadena debe liberarse mediante [**MpFreeMemory.**](mpfreememory.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**.

Si se produce un error en la función, el valor devuelto es un **código HRESULT** con errores.

## <a name="remarks"></a>Comentarios

Esta función es capaz de aplicar formato a los códigos de error del sistema además de códigos de error específicos devueltos por las funciones de protección contra malware. Los códigos de error **HRESULT** específicos de las funciones de protección contra malware tienen una 0x50. A continuación se muestra una lista de un subconjunto de los códigos de error específicos de la protección contra malware que pueden devolver varias funciones de protección contra malware. Con la macro **HRESULT \_ FROM MP \_ \_ STATUS**, los siguientes códigos de error se pueden convertir en **HRESULT**. Consulte también [Códigos de error del motor antimalware](https://support.microsoft.com/kb/939359) de Forefront Client Security para obtener una lista de otros códigos de error posibles.



| Código de error                              | Descripción                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| ERROR \_ MP \_ NOENGINE                     | No se carga ningún motor en el servicio antimalware para realizar la operación solicitada.                                              |
| ERROR \_ MP \_ NO \_ MEMORY                   | El motor antimalware no ha encontrado ninguna situación de memoria.                                                               |
| ERROR \_ AL QUITAR EL \_ MP \_               | Error en la operación de eliminación de una amenaza específica.                                                                              |
| ERROR AL \_ PONER EN CUARENTENA EL \_ MP \_           | Error en la operación de cuarentena para una amenaza específica.                                                                          |
| ERROR \_ NO SE ENCONTRÓ LA AMENAZA DE \_ \_ MP \_           | La amenaza específica ya no existe en el sistema.                                                                         |
| NO \_ SE ADMITE LA \_ \_ ELIMINACIÓN DE MP DE \_ ERROR       | No se admite la operación de eliminación de una amenaza específica dentro del tipo de contenedor.                                          |
| ERROR \_ MP \_ REMOVE \_ IMMUTABLE \_ CONTAINER | Debido a la directiva del motor, no se admite una operación de eliminación de una amenaza específica dentro de un contenedor bloqueado. (Archivos de correo). |
| ERROR \_ MP \_ BADDB \_ OLDENGINE             | La solicitud de actualización de firma proporcionaba un motor o archivos de firma más antiguos.                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpManagerAbrir**](mpmanageropen.md)
</dt> <dt>

[Códigos de error del motor antimalware de Forefront Client Security](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 






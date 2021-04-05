---
title: Función MpErrorMessageFormat (MpClient. h)
description: Devuelve un mensaje de error con formato basado en un código de error.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Función MpErrorMessageFormat características de entorno heredado de Windows
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
ms.openlocfilehash: 3a3499b3be885b29135d22b470da4143cfb23ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996969"
---
# <a name="mperrormessageformat-function"></a>MpErrorMessageFormat función)

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

*hMpHandle* \[ de\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*hrError* \[ de\]
</dt> <dd>

Tipo: **HRESULT**

Un código de error basado en **HRESULT**.

</dd> <dt>

*pwszErrorDesc* \[ enuncia\]
</dt> <dd>

Tipo: **LPWStr \** _

Devuelve un mensaje de error con formato basado en _hrError *. Esta cadena se debe liberar mediante [**MpFreeMemory**](mpfreememory.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.

Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.

## <a name="remarks"></a>Observaciones

Esta función es capaz de dar formato a los códigos de error del sistema, además de códigos de error específicos devueltos por las funciones de protección contra malware. Los códigos de error **HRESULT** específicos de las funciones de protección contra malware tienen una instalación de 0x50. A continuación se muestra una lista de un subconjunto de códigos de error específicos de protección contra malware que pueden ser devueltos por diversas funciones de protección contra malware. Con la macro **HRESULT \_ del \_ \_ Estado de MP**, los siguientes códigos de error se pueden convertir en **HRESULT**. Vea también [códigos de error del motor de antimalware de Forefront Client Security](https://support.microsoft.com/kb/939359) para obtener una lista de otros códigos de error posibles.



| Código de error                              | Descripción                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| ERROR de procesador \_ MP \_                     | No se ha cargado ningún motor en el servicio antimalware para realizar la operación solicitada.                                              |
| ERROR de \_ MP \_ sin \_ memoria                   | El motor de antimalware ha encontrado una situación de falta de memoria.                                                               |
| ERROR de \_ eliminación del módulo de administración \_ \_               | No se pudo realizar la operación de eliminación de una amenaza concreta.                                                                              |
| ERROR de \_ cuarentena del módulo de administración \_ \_           | No se pudo realizar la operación de cuarentena para una amenaza concreta.                                                                          |
| \_ \_ \_ no \_ se encontró la amenaza del módulo de administración           | La amenaza específica ya no existe en el sistema.                                                                         |
| ERROR \_ al \_ quitar MP \_ no \_ compatible       | No se admite la operación de eliminación de una amenaza concreta dentro del tipo de contenedor.                                          |
| ERROR de \_ MP \_ quitar \_ contenedor inmutable \_ | Debido a la Directiva del motor, no se admite una operación de eliminación de una amenaza específica dentro de un contenedor bloqueado. (Archivos de correo electrónico). |
| ERROR \_ MP \_ BADDB \_ OLDENGINE             | La solicitud de actualización de firma proporcionó un motor o archivos de firma antiguos.                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[Códigos de error del motor de antimalware de Forefront Client Security](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 






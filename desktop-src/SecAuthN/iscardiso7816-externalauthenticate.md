---
description: Construye un comando APDU (unidad de datos de protocolo de aplicación) que actualiza condicionalmente el estado de seguridad, comprobando la identidad del equipo cuando la tarjeta inteligente no confía en él.
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'ISCardISO7816:: ExternalAuthenticate (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423819"
---
# <a name="iscardiso7816externalauthenticate-method"></a>ISCardISO7816:: ExternalAuthenticate (método)

\[El método **ExternalAuthenticate** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **ExternalAuthenticate** crea un comando APDU ( [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) ) que actualiza condicionalmente el estado de seguridad, comprobando la identidad del equipo cuando la [*tarjeta inteligente*](../secgloss/s-gly.md) no confía en él.

El comando usa el resultado (sí o no) del cálculo de la tarjeta (según un desafío emitido anteriormente por la tarjeta, por ejemplo, mediante el \_ comando ins Get \_ Challenge), una clave (posiblemente secreta) almacenada en la tarjeta y los datos de autenticación transmitidos por el dispositivo de interfaz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byAlgorithmRef* \[ de\]
</dt> <dd>

Referencia del algoritmo en la tarjeta.

Si este valor es cero, indica que no se proporciona información. La referencia del algoritmo se conoce antes de emitir el comando o se proporciona en el campo de datos.

</dd> <dt>

*bySecretRef* \[ de\]
</dt> <dd>

Referencia del secreto.



| Value                                                                                                                                                                                    | Significado                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Sin información**</dt> </dl>                     | Posición de bit: 00000000<br/> No se proporciona información. La referencia del secreto se conoce antes de emitir el comando o se proporciona en el campo de datos.<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Referencia global**</dt> </dl>         | Posición de bit: 0-------<br/> Datos de referencia global (una clave específica de MF).<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Referencia específica**</dt> </dl> | Posición de bit: 1-------<br/> Datos de referencia específicos (una clave específica de DF).<br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Posición de bit:-XX-----<br/> 00 (otros valores son RFU).<br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Secreto**</dt> </dl>                         | Posición de bit:---xxxxx<br/> Número del secreto.<br/>                                                                                                             |



 

</dd> <dt>

*pChallenge* \[ de\]
</dt> <dd>

Puntero a los datos relacionados con la autenticación. Este parámetro puede ser **null**.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.

En la devolución, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | La operación se ha completado correctamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Se pasó un parámetro no válido.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido.<br/>              |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                            |



 

## <a name="remarks"></a>Observaciones

Para que el comando encapsulado se realice correctamente, el último desafío Obtenido de la tarjeta debe ser válido.

Las comparaciones erróneas se pueden grabar en la tarjeta (por ejemplo, para limitar el número de intentos adicionales de uso de los datos de referencia).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 

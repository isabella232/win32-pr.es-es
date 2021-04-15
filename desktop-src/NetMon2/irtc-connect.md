---
description: El método Connect conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'IRTC:: Connect (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a14e34aeb0be30165aa18ddc7da18028d715be01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677348"
---
# <a name="irtcconnect-method"></a>IRTC:: Connect (método)

El método **Connect** conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hInputBlob* \[ de\]
</dt> <dd>

Identificador del BLOB que especifica la NIC a la que se está conectando y la información de configuración para esa conexión.

</dd> <dt>

*StatusCallbackProc* \[ de\]
</dt> <dd>

Dirección de la función de devolución de llamada de estado del usuario, que recibe actualizaciones de estado, como los desencadenadores. Este parámetro se puede establecer en **null**.

</dd> <dt>

*FramesCallbackProc* \[ de\]
</dt> <dd>

Dirección de la función de devolución de llamada de fotograma del usuario, que se usa para recibir actualizaciones de estado como los desencadenadores. Este parámetro se puede establecer en **null**.

</dd> <dt>

*UserContext* \[ de\]
</dt> <dd>

Valor que se pasa cuando se llama a la función de devolución de llamada del marco y el estado del usuario. Si se especifican ambas funciones de devolución de llamada, deben usar el mismo valor de contexto de usuario. El valor de este parámetro suele ser HWND o un puntero ' this '.

</dd> <dt>

*hErrorBlob* \[ enuncia\]
</dt> <dd>

Identificador de un BLOB de error que contiene información de error adicional. Vea la sección Comentarios en la parte inferior de este tema para obtener información sobre lo que hay en el BLOB de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por la llamada interna **IRTC:: configure** ):



| Código devuelto                                                                                                         | Descripción                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ ya \_ conectado**</dt> </dl>            | Esta instancia del objeto COM NPP ya está conectada a la red.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**\_error de \_ conversión de BLOB NMERR \_**</dt> </dl>       | El BLOB de configuración está dañado. Este error se genera mediante la llamada a **IRTC:: configure** .<br/>                                                                                                                                                                                       |
| <dl> <dt>**la \_ entrada de BLOB NMERR \_ \_ \_ no \_ existe**</dt> </dl> | Falta una entrada necesaria para realizar esta operación en el BLOB de entrada especificado por el parámetro *hInputBlob* . Este error puede generarse mediante la llamada a **IRTC:: Connect** o **IRTC:: configure** . Observe el BLOB de error devuelto por *hErrorBlob* para determinar qué entrada no se encontró.<br/> |
| <dl> <dt>**\_BLOB NMERR \_ no \_ inicializado**</dt> </dl>        | No se ha llamado a la función **CreateBlob** . Este error se genera mediante la llamada a **IRTC:: configure** .<br/>                                                                                                                                                                         |
| <dl> <dt>**NMERR \_ cadena de blob \_ \_ no válida**</dt> </dl>         | La cadena no termina en NULL. Este error se genera mediante la llamada a **IRTC:: configure** .<br/>                                                                                                                                                                                       |
| <dl> <dt>**\_desencadenador no válido de NMERR \_**</dt> </dl>              | La parte del desencadenador del BLOB de entrada está dañada. Este error se genera mediante la llamada a **IRTC:: configure** .<br/>                                                                                                                                                                        |
| <dl> <dt>**NMERR \_ BLOB no válido \_**</dt> </dl>                 | El objeto especificado en *hInputBlob* no es un BLOB. Este error se genera mediante la llamada a **IRTC:: configure** .<br/>                                                                                                                                                                      |
| <dl> <dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt> </dl>               | La memoria necesaria para realizar esta operación no está disponible. Este error se genera mediante la llamada a **IRTC:: configure** .<br/>                                                                                                                                                              |
| <dl> <dt>**tiempo de espera de NMERR \_**</dt> </dl>                       | La solicitud ha agotado el tiempo de espera. Este error se genera mediante la llamada a **IRTC:: configure** .<br/>                                                                                                                                                                                               |
| <dl> <dt>**\_BLOB de nivel superior de NMERR \_**</dt> </dl>                 | El número de versión del BLOB especificado en *hInputBlob* es incorrecto. Este error se genera mediante la llamada a **IRTC:: configure** .<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Observaciones

Cuando se llama al método **Connect** , el NPP llama automáticamente al método **IRTC:: configure** mediante el BLOB proporcionado por *hInputBlob*. Tenga en cuenta que los códigos de error devueltos por la llamada a **IRTC:: configure** se devuelven y se devuelven mediante la llamada a **IRTC:: Connect** .

Se debe llamar a este método antes de poder iniciar la captura de fotogramas. Tenga en cuenta que cuando se conecta a la red mediante este método, debe seguir usando la interfaz **IRTC** para capturar fotogramas.

Al llamar a esta función, debe especificar una función de devolución de llamada de estado o de fotograma, incluso si solo actúa como marcador de posición.

El BLOB de entrada especificado por *hInputBlob* se puede obtener llamando a los métodos **GetNPPBlobFromUI**, **GetNPPBlobTable** y **SelectNPPBlobFromTable** .

El BLOB de error devuelto en *hErrorBlob* contiene información de error que el desarrollador o la aplicación pueden usar para solucionar problemas. El BLOB de error devuelto por *hErrorBlob* contiene entradas que monitor de red no pudo comprender o encontrar en el BLOB de entrada especificado en *hInputBlob*. Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada monitor de red no encontró se incluye en el BLOB de error devuelto.



| Para información acerca de                          | Vea                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Obtener el BLOB de entrada que representa una NIC | [Seleccionar una tarjeta de interfaz de red](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: configure](irtc-configure.md)
</dt> <dt>

[IRTC::D Ulta](irtc-disconnect.md)
</dt> <dt>

[IRTC:: Start](irtc-start.md)
</dt> </dl>

 

 





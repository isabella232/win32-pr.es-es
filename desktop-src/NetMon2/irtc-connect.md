---
description: 'Método IRTC::Conectar: el método Conectar conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.'
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: Método IRTC::Conectar (Netmon.h)
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
ms.openlocfilehash: ba62f3341b18ddfdbf09af4eec701322d901ab79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169285"
---
# <a name="irtcconnect-method"></a>IRTC::Conectar método

El **Conectar** conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.

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

*hInputBlob* \[ En\]
</dt> <dd>

Controle el BLOB que especifica la NIC a la que se va a conectar y la información de configuración de esa conexión.

</dd> <dt>

*StatusCallbackProc* \[ En\]
</dt> <dd>

Dirección de la función de devolución de llamada de estado del usuario, que recibe actualizaciones de estado como desencadenadores. Este parámetro se puede establecer en **NULL.**

</dd> <dt>

*FramesCallbackProc* \[ En\]
</dt> <dd>

Dirección de la función de devolución de llamada de marco del usuario, que se usa para recibir actualizaciones de estado, como desencadenadores. Este parámetro se puede establecer en **NULL.**

</dd> <dt>

*UserContext* \[ En\]
</dt> <dd>

Valor pasado cuando se llama al estado del usuario y a la función de devolución de llamada de marco. Si se especifican ambas funciones de devolución de llamada, deben usar el mismo valor de contexto de usuario. El valor de este parámetro suele ser HWND o un puntero "this".

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Controlar un blob de error que contiene información de error adicional. Vea Comentarios en la parte inferior de este tema para obtener información sobre lo que hay en el blob de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por la llamada **interna IRTC::Configure):**



| Código devuelto                                                                                                         | Descripción                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ YA \_ CONECTADO**</dt> </dl>            | Esta instancia del objeto COM de NPP ya está conectada a la red.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**ERROR DE CONVERSIÓN \_ DE \_ BLOBS DE NMERR \_**</dt> </dl>       | El BLOB de configuración está dañado. La llamada **IRTC::Configure** genera este error.<br/>                                                                                                                                                                                       |
| <dl> <dt>**LA ENTRADA DE BLOB DE NMERR \_ \_ NO \_ \_ \_ EXISTE**</dt> </dl> | El BLOB de entrada especificado por el *parámetro hInputBlob* carece de una entrada necesaria para realizar esta operación. La llamada **IRTC::Conectar** **o IRTC::Configure** puede generar este error. Mire el blob de error devuelto por *hErrorBlob para* determinar qué entrada no se encontró.<br/> |
| <dl> <dt>**BLOB DE NMERR \_ \_ NO \_ INICIALIZADO**</dt> </dl>        | No se ha llamado a la función **CreateBlob.** La llamada **IRTC::Configure** genera este error.<br/>                                                                                                                                                                         |
| <dl> <dt>**CADENA DE BLOB DE NMERR \_ \_ NO \_ VÁLIDA**</dt> </dl>         | La cadena no termina en NULL. La llamada **IRTC::Configure** genera este error.<br/>                                                                                                                                                                                       |
| <dl> <dt>**DESENCADENADOR NO ES DE NMERR \_ \_**</dt> </dl>              | La parte del desencadenador del BLOB de entrada está dañada. La llamada **IRTC::Configure** genera este error.<br/>                                                                                                                                                                        |
| <dl> <dt>**BLOB NO VÁLIDO DE NMERR \_ \_**</dt> </dl>                 | El objeto especificado en *hInputBlob* no es un BLOB. La llamada **IRTC::Configure** genera este error.<br/>                                                                                                                                                                      |
| <dl> <dt>**MEMORIA DE NMERR \_ \_ FUERA DE LA \_ MEMORIA**</dt> </dl>               | La memoria necesaria para realizar esta operación no está disponible. La llamada **IRTC::Configure** genera este error.<br/>                                                                                                                                                              |
| <dl> <dt>**TIEMPO DE ESPERA de NMERR \_**</dt> </dl>                       | Se ha producido un tiempo de espera de la solicitud. La llamada **IRTC::Configure** genera este error.<br/>                                                                                                                                                                                               |
| <dl> <dt>**BLOB DE \_ NMERR UPLEVEL \_**</dt> </dl>                 | El número de versión del BLOB especificado en *hInputBlob* es incorrecto. La llamada **IRTC::Configure** genera este error.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Observaciones

Cuando se **Conectar** al método , el NPP llama automáticamente al método **IRTC::Configure** mediante el BLOB proporcionado por *hInputBlob*. Tenga en cuenta que los códigos de error devueltos por la llamada a **IRTC::Configure** se devuelven y devuelve la llamada **IRTC::Conectar.**

Se debe llamar a este método para poder empezar a capturar fotogramas. Tenga en cuenta que al conectarse a la red mediante este método, debe seguir usando la **interfaz IRTC** para capturar fotogramas.

Al llamar a esta función, debe especificar una función de devolución de llamada de estado o marco, incluso si solo actúa como marcador de posición.

El BLOB de entrada especificado por *hInputBlob* se puede obtener llamando a los métodos **GetNPPBlobFromUI,** **GetNPPBlobTable** y **SelectNPPBlobFromTable.**

El BLOB de error devuelto en *hErrorBlob* contiene información de error que el desarrollador o la aplicación pueden usar para solucionar problemas. El blob de error devuelto por *hErrorBlob* contiene entradas que Monitor de red no se pudieron entender ni encontrar en el BLOB de entrada especificado en *hInputBlob*. Por ejemplo, si se devuelve NMERR BLOB ENTRY DOES NOT EXIST, la entrada Monitor de red no se encuentra se incluye en el \_ \_ blob de error \_ \_ \_ devuelto.



| Para información acerca de                          | Vea                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Obtención del BLOB de entrada que representa una NIC | [Selección de una tarjeta de interfaz de red](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Configure](irtc-configure.md)
</dt> <dt>

[IRTC::D isconnect](irtc-disconnect.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> </dl>

 

 





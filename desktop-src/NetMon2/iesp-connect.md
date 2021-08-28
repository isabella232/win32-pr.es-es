---
description: El Conectar conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración sobre la conexión.
ms.assetid: 48189b2b-9889-4bd8-8972-26005fb7c341
title: Método IESP::Conectar (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9383b6d7638df89bebd369a3657283c1fd6b56ac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480151"
---
# <a name="iespconnect-method"></a>IESP::Conectar método

El **Conectar** conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración sobre la conexión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB hInputBlob,
  [in]  DWORD StatusCallbackProc,
  [in]  DWORD UserContext,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hInputBlob* \[ En\]
</dt> <dd>

Controle el BLOB que especifica la NIC a la que se conecta el NPP y la información de configuración de esa conexión.

</dd> <dt>

*StatusCallbackProc* \[ En\]
</dt> <dd>

Dirección de la función de devolución de llamada del usuario, que recibe actualizaciones de estado, como desencadenadores. Si no se usa una función de devolución de llamada, establezca este parámetro y el *parámetro UserContext* en **NULL.**

</dd> <dt>

*UserContext* \[ En\]
</dt> <dd>

Valor pasado cuando se llama a la función de devolución de llamada del usuario. El valor de este parámetro suele ser HWND o un puntero "this". Si no se especifica una función de devolución de llamada, establezca este parámetro y el *parámetro StatusCallbackProc* en **NULL.**

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Controlar un blob de error que contiene información de error adicional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por la llamada **interna IESP::Configure):**




| Código devuelto | Descripción | 
|-------------|-------------|
| <dl><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt></dl> | Esta instancia del objeto COM de NPP ya está conectada a la red.<br /> | 
| <dl><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt></dl> | El BLOB de configuración está dañado. Este error lo genera la <strong>llamada IESP::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt></dl> | El BLOB de entrada especificado por el <em>parámetro hInputBlob</em> carece de una entrada necesaria para realizar esta operación. Este error puede generarse mediante la <strong>llamada IESP::Conectar</strong> <strong>o IESP::Configure.</strong> Mire el blob de error devuelto por <em>hErrorBlob para</em> determinar qué entrada no se encontró.<br /> | 
| <dl><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt></dl> | No se ha llamado a la función <strong>CreateBlob.</strong> Este error lo genera la <strong>llamada IESP::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt></dl> | La cadena no termina en NULL. Este error lo genera la <strong>llamada IESP::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt></dl> | La parte del desencadenador del BLOB de entrada está dañada. Este error lo genera la <strong>llamada IESP::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_INVALID_BLOB</strong></dt></dl> | El objeto especificado en <em>hInputBlob</em> no es un BLOB. Este error lo genera la <strong>llamada IESP::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt></dl> | El directorio de captura predeterminado no se estableció en el Registro. Use la ruta de acceso siguiente para establecer el directorio de captura. <br /><pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre> | 
| <dl><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt></dl> | La memoria necesaria para realizar esta operación no está disponible. Este error lo genera la <strong>llamada IESP::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_TIMEOUT</strong></dt></dl> | Se ha producido un tiempo de espera de la solicitud. Este error lo genera la <strong>llamada IESP::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt></dl> | El número de versión del BLOB especificado en <em>hInputBlob</em> es incorrecto. Este error lo genera la <strong>llamada IESP::Configure.</strong><br /> | 




 

## <a name="remarks"></a>Comentarios

Cuando se **Conectar** al método Monitor de red, llama automáticamente a **IESP::Configure** mediante el BLOB proporcionado por el *parámetro hInputBlob.* Tenga en cuenta que los códigos de error devueltos por la llamada a **IESP::Configure** se devuelven y devuelve la **llamada IESP::Conectar.**

Se debe llamar a este método para poder empezar a capturar fotogramas. Tenga en cuenta que al conectarse a la red mediante este método, debe seguir usando la **interfaz IESP** para capturar fotogramas.

El BLOB de entrada especificado por *hInputBlob* se puede obtener llamando a **GetNPPBlobFromUI,** **GetNPPBlobTable** y **SelectNPPBlobFromTable.**

El blob de error devuelto por *hErrorBlob* contiene entradas que Monitor de red no se pudieron entender ni encontrar en el BLOB de entrada especificado en *hInputBlob*. El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas. Por ejemplo, si se devuelve NMERR BLOB ENTRY DOES NOT EXIST, la entrada que Monitor de red no se pudo encontrar se incluye en el \_ \_ blob de error \_ \_ \_ devuelto.



| Para información acerca de                          | Vea                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Obtención del BLOB de entrada que representa una NIC | [Selección de una tarjeta de interfaz de red](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Configure](iesp-configure.md)
</dt> <dt>

[IESP::D isconnect](iesp-disconnect.md)
</dt> <dt>

[IESP::Start](iesp-start.md)
</dt> </dl>

 

 





---
description: El Conectar conecta el NPP a la red mediante una tarjeta de interfaz de red especificada y proporciona información de configuración sobre la conexión.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: Método IDelaydC::Conectar (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e91db1dae0c67c5f35e46841867d3d3e15058cf0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476736"
---
# <a name="idelaydcconnect-method"></a>IDelaydC::Conectar método

El **Conectar** conecta el NPP a la red mediante una tarjeta de interfaz de red especificada y proporciona información de configuración sobre la conexión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hInputBlob* \[ En\]
</dt> <dd>

Controle el BLOB que especifica la NIC a la que se va a conectar y la información de configuración sobre esa conexión.

</dd> <dt>

*StatusCallbackProc* \[ En\]
</dt> <dd>

Dirección de la función de devolución de llamada del usuario, que se usa para recibir actualizaciones de estado, como desencadenadores. Si no se usa ninguna función de devolución de llamada, establezca este parámetro y el *parámetro UserContext* en **NULL.**

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

Si este método se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por la llamada **interna IDelaydC::Configure):**




| Código devuelto | Descripción | 
|-------------|-------------|
| <dl><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt></dl> | Esta instancia del objeto COM de NPP ya está conectada a la red.<br /> | 
| <dl><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt></dl> | El BLOB de configuración está dañado. La llamada a <strong>IDelaydC::Configure</strong> genera este error.<br /> | 
| <dl><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt></dl> | Al BLOB de entrada especificado por <em>hInputBlob</em> le falta una entrada necesaria para realizar esta operación. Este error lo pueden generar las llamadas <strong>IDelaydC::Conectar</strong> <strong>o IDelaydC::Configure.</strong> Mire el blob de error devuelto por <em>hErrorBlob para</em> determinar qué entrada no se encontró.<br /> | 
| <dl><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt></dl> | No se ha llamado a la función <strong>CreateBlob.</strong> La llamada a <strong>IDelaydC::Configure</strong> genera este error.<br /> | 
| <dl><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt></dl> | La cadena no termina en NULL. La llamada a <strong>IDelaydC::Configure</strong> genera este error.<br /> | 
| <dl><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt></dl> | La parte del desencadenador del BLOB de entrada está dañada. La llamada a <strong>IDelaydC::Configure</strong> genera este error.<br /> | 
| <dl><dt><strong>NMERR_INVALID_BLOB</strong></dt></dl> | El objeto especificado en <em>hInputBlob</em> no es un BLOB. La llamada a <strong>IDelaydC::Configure</strong> genera este error.<br /> | 
| <dl><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt></dl> | El directorio de captura predeterminado no se estableció en el Registro. Use la ruta de acceso siguiente para establecer el directorio de captura. <br /><pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre> | 
| <dl><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt></dl> | No había memoria disponible para realizar esta operación. La llamada a <strong>IDelaydC::Configure</strong> genera este error.<br /> | 
| <dl><dt><strong>NMERR_TIMEOUT</strong></dt></dl> | Se ha producido un tiempo de espera de la solicitud. Este error lo genera la <strong>llamada IDelaydC::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt></dl> | El número de versión del BLOB especificado en <em>hInputBlob</em> es incorrecto. La llamada a <strong>IDelaydC::Configure</strong> genera este error.<br /> | 




 

## <a name="remarks"></a>Observaciones

Cuando se **Conectar** al método , el NPP llama automáticamente a **IDelaydC::Configure** mediante el BLOB proporcionado por *hInputBlob*. Tenga en cuenta que los códigos de error devueltos por la llamada a **IDelaydC::Configure** se devuelven y se devuelven mediante la llamada **a IDelaydC::Conectar** llamada.

Se debe llamar a este método para poder empezar a capturar fotogramas. Tenga en cuenta que al conectarse a la red mediante este método, debe seguir usando los métodos de interfaz **IDelaydC** para capturar fotogramas.

El BLOB de entrada especificado por el parámetro *hInputBlob* se puede obtener llamando a **GetNPPBlobFromUI,** **GetNPPBlobTable** y **SelectNPPBlobFromTable.**

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

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC::D isconnect](idelaydc-disconnect.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> </dl>

 

 





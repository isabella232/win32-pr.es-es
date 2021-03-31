---
description: El método Connect conecta el NPP a la red mediante una tarjeta de interfaz de red especificada y proporciona información de configuración sobre la conexión.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: 'IDelaydC:: Connect (método) (Netmon. h)'
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
ms.openlocfilehash: b2cd1fb5ad694493c4a225aa3bf109d7775b9dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907665"
---
# <a name="idelaydcconnect-method"></a>IDelaydC:: Connect (método)

El método **Connect** conecta el NPP a la red mediante una tarjeta de interfaz de red especificada y proporciona información de configuración sobre la conexión.

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

*hInputBlob* \[ de\]
</dt> <dd>

Identificador del BLOB que especifica la NIC a la que se está conectando y la información de configuración sobre dicha conexión.

</dd> <dt>

*StatusCallbackProc* \[ de\]
</dt> <dd>

Dirección de la función de devolución de llamada del usuario, que se usa para recibir las actualizaciones de estado como los desencadenadores. Si no se usa ninguna función de devolución de llamada, establezca este parámetro y el parámetro *UserContext* en **null**.

</dd> <dt>

*UserContext* \[ de\]
</dt> <dd>

Valor que se pasa cuando se llama a la función de devolución de llamada del usuario. El valor de este parámetro suele ser HWND o un puntero ' this '. Si no se especifica una función de devolución de llamada, establezca este parámetro y el parámetro *StatusCallbackProc* en **null**.

</dd> <dt>

*hErrorBlob* \[ enuncia\]
</dt> <dd>

Identificador de un BLOB de error que contiene información de error adicional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por la llamada interna **IDelaydC:: configure** ):



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código devuelto</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </dl></td>
<td>Esta instancia del objeto COM NPP ya está conectada a la red.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </dl></td>
<td>El BLOB de configuración está dañado. Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </dl></td>
<td>Falta una entrada necesaria para realizar esta operación en el BLOB de entrada especificado por <em>hInputBlob</em> . Este error puede generarse mediante la llamada a <strong>IDelaydC:: Connect</strong> o <strong>IDelaydC:: configure</strong> . Observe el BLOB de error devuelto por <em>hErrorBlob</em> para determinar qué entrada no se encontró.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </dl></td>
<td>No se ha llamado a la función <strong>CreateBlob</strong> . Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </dl></td>
<td>La cadena no termina en NULL. Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </dl></td>
<td>La parte del desencadenador del BLOB de entrada está dañada. Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_INVALID_BLOB</strong></dt> </dl></td>
<td>El objeto especificado en <em>hInputBlob</em> no es un BLOB. Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </dl></td>
<td>No se estableció el directorio de captura predeterminado en el registro. Use la siguiente ruta de acceso para establecer el directorio de captura. <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </dl></td>
<td>No había memoria disponible para realizar esta operación. Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_TIMEOUT</strong></dt> </dl></td>
<td>La solicitud ha agotado el tiempo de espera. Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </dl></td>
<td>El número de versión del BLOB especificado en <em>hInputBlob</em> es incorrecto. Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Cuando se llama al método **Connect** , el NPP llama automáticamente a **IDelaydC:: configure** mediante el BLOB proporcionado por *hInputBlob*. Tenga en cuenta que los códigos de error devueltos por la llamada a **IDelaydC:: configure** se devuelven y se devuelven mediante la llamada a **IDelaydC:: Connect** .

Se debe llamar a este método antes de poder iniciar la captura de fotogramas. Tenga en cuenta que cuando se conecta a la red mediante este método, debe seguir usando los métodos de la interfaz **IDelaydC** para capturar fotogramas.

El BLOB de entrada especificado por el parámetro *hInputBlob* se puede obtener llamando a **GetNPPBlobFromUI**, **GetNPPBlobTable** y **SelectNPPBlobFromTable**.

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

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC:: configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC::D Ulta](idelaydc-disconnect.md)
</dt> <dt>

[IDelaydC:: Start](idelaydc-start.md)
</dt> </dl>

 

 





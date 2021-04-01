---
description: El método Connect conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: 'IStas:: Connect (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7705600c3ce68b719014c928ac4d02c62cba64cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913854"
---
# <a name="istatsconnect-method"></a>IStas:: Connect (método)

El método **Connect** conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.

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

Identificador del BLOB que especifica la NIC a la que se conecta el NPP y la información de configuración para esa conexión.

</dd> <dt>

*StatusCallbackProc* \[ de\]
</dt> <dd>

Dirección de la función de devolución de llamada del usuario, que recibe actualizaciones de estado, como los desencadenadores. Si no se utiliza una función de devolución de llamada, establezca este parámetro y el parámetro *UserContext* en **null**.

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

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por las llamadas internas **:: configure** ):



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
<td>El BLOB de configuración está dañado. Este error lo genera la llamada a la función <strong>istas:: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </dl></td>
<td>Falta una entrada necesaria para realizar esta operación en el BLOB de entrada especificado por el parámetro <em>hInputBlob</em> . Este error lo puede generar la llamada a los <strong>istas:: Connect</strong> o <strong>istas:: configure</strong> . Observe el BLOB de error devuelto por <em>hErrorBlob</em> para determinar qué entrada no se encontró.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </dl></td>
<td>No se ha llamado a la función <strong>CreateBlob</strong> . Este error lo genera la llamada a la función <strong>istas:: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </dl></td>
<td>La cadena no termina en NULL. Este error lo genera la llamada a la función <strong>istas:: configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </dl></td>
<td>La parte del desencadenador del BLOB de entrada está dañada. Este error lo genera la llamada a la función <strong>istas:: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_INVALID_BLOB</strong></dt> </dl></td>
<td>El objeto especificado en <em>hInputBlob</em> no es un BLOB. Este error lo genera la llamada a la función <strong>istas:: configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </dl></td>
<td>No se estableció el directorio de captura predeterminado en el registro. Para establecer el directorio de captura, use la siguiente ruta de acceso. <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </dl></td>
<td>La memoria necesaria para realizar esta operación no estaba disponible. Este error lo genera la llamada a la función <strong>istas:: configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_TIMEOUT</strong></dt> </dl></td>
<td>La solicitud ha agotado el tiempo de espera. Este error lo genera la llamada a la función <strong>istas:: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </dl></td>
<td>El número de versión del BLOB especificado en <em>hInputBlob</em> es incorrecto. Este error lo genera la llamada a la función <strong>istas:: configure</strong> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Cuando se llama al método **Connect** , monitor de red llama automáticamente al método **istas:: configure** mediante el BLOB proporcionado por el parámetro *hInputBlob* . Tenga en cuenta que los códigos de error devueltos por la llamada a los **ISTA:: configure** se devuelven y se devuelven mediante la llamada a los **ISTA:: Connect** .

Se debe llamar a este método antes de poder iniciar la captura de fotogramas. Tenga en cuenta que cuando se conecta a la red mediante este método, debe seguir usando la interfaz **istas** para capturar fotogramas.

El BLOB de entrada especificado por *hInputBlob* se puede obtener llamando a los métodos **GetNPPBlobFromUI**, **GetNPPBlobTable** y **SelectNPPBlobFromTable** .

El BLOB de error devuelto por el parámetro *hErrorBlob* contiene entradas que monitor de red no pudieron comprender o encontrar en el BLOB de entrada especificado en *hInputBlob*. El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas. Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada que monitor de red no pudo encontrar se incluye en el BLOB de error devuelto.



| Para información acerca de                                             | Vea                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Obtener el BLOB de entrada que representa una tarjeta de interfaz de red | [Seleccionar una tarjeta de interfaz de red](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IStas](istats.md)
</dt> <dt>

[ISta:: configurar](istats-configure.md)
</dt> <dt>

[IStas::D Ulta](istats-disconnect.md)
</dt> <dt>

[BLOBs Monitor de red](network-monitor-blobs.md)
</dt> </dl>

 

 





---
description: 'Método IStats::Connect: el método Connect conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.'
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: Método IStats::Connect (Netmon.h)
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
ms.openlocfilehash: 0719b6ff56aaa8c0be02f86d62ac23d4003aa3d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098483"
---
# <a name="istatsconnect-method"></a>IStats::Connect (método)

El **método Connect** conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.

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

Controle el BLOB que especifica la NIC a la que se conecta el NPP y la información de configuración de esa conexión.

</dd> <dt>

*StatusCallbackProc* \[ En\]
</dt> <dd>

Dirección de la función de devolución de llamada del usuario, que recibe actualizaciones de estado como desencadenadores. Si no se usa una función de devolución de llamada, establezca este parámetro y el *parámetro UserContext* en **NULL.**

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

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por la llamada **interna IStats::Configure):**



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
<td>Esta instancia del objeto COM de NPP ya está conectada a la red.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </dl></td>
<td>El BLOB de configuración está dañado. La llamada a <strong>IStats::Configure</strong> genera este error.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </dl></td>
<td>El BLOB de entrada especificado por el <em>parámetro hInputBlob</em> carece de una entrada necesaria para realizar esta operación. Este error puede generarse mediante la <strong>llamada IStats::Connect</strong> o <strong>IStats::Configure.</strong> Mire el blob de error devuelto por <em>hErrorBlob para</em> determinar qué entrada no se encontró.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </dl></td>
<td>No se ha llamado a la función <strong>CreateBlob.</strong> La llamada a <strong>IStats::Configure</strong> genera este error.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </dl></td>
<td>La cadena no termina en NULL. La llamada a <strong>IStats::Configure</strong> genera este error.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </dl></td>
<td>La parte del desencadenador del BLOB de entrada está dañada. La llamada a <strong>IStats::Configure</strong> genera este error.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_INVALID_BLOB</strong></dt> </dl></td>
<td>El objeto especificado en <em>hInputBlob</em> no es un BLOB. La llamada a <strong>IStats::Configure</strong> genera este error.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </dl></td>
<td>El directorio de captura predeterminado no se estableció en el Registro. Para establecer el directorio de captura, use la ruta de acceso siguiente. <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </dl></td>
<td>La memoria necesaria para realizar esta operación no estaba disponible. La llamada a <strong>IStats::Configure</strong> genera este error.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_TIMEOUT</strong></dt> </dl></td>
<td>Se ha pasado el tiempo de espera de la solicitud. La llamada a <strong>IStats::Configure</strong> genera este error.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </dl></td>
<td>El número de versión del BLOB especificado en <em>hInputBlob</em> es incorrecto. La llamada a <strong>IStats::Configure</strong> genera este error.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentarios

Cuando se llama al método **Connect,** Monitor de red llama automáticamente al método **IStats::Configure** mediante el blob proporcionado por el *parámetro hInputBlob.* Tenga en cuenta que los códigos de error devueltos por la llamada a **IStats::Configure** se devuelven y devuelven mediante la **llamada IStats::Connect.**

Se debe llamar a este método para poder empezar a capturar fotogramas. Tenga en cuenta que cuando se conecta a la red mediante este método, debe seguir usando la **interfaz IStats** para capturar fotogramas.

El BLOB de entrada especificado por *hInputBlob* se puede obtener llamando a los métodos **GetNPPBlobFromUI**, **GetNPPBlobTable** y **SelectNPPBlobFromTable.**

El blob de error devuelto por el parámetro *hErrorBlob* contiene entradas que Monitor de red no se pudieron comprender o encontrar en el BLOB de entrada especificado en *hInputBlob*. El blob de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas. Por ejemplo, si se devuelve NMERR BLOB ENTRY DOES NOT EXIST, la entrada que no Monitor de red encuentra se incluye en el \_ \_ blob de error \_ \_ \_ devuelto.



| Para información acerca de                                             | Vea                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Obtención del BLOB de entrada que representa una tarjeta de interfaz de red | [Selección de una tarjeta de interfaz de red](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Configure](istats-configure.md)
</dt> <dt>

[IStats::D isconnect](istats-disconnect.md)
</dt> <dt>

[Monitor de red BLOBS](network-monitor-blobs.md)
</dt> </dl>

 

 





---
description: Elimina la clase o instancia especificada en la ruta de acceso del objeto.
ms.assetid: f5ed170e-d002-4dd9-b8b6-b764a7a41a27
ms.tgt_platform: multiple
title: Método SWbemServices.DeleteAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bcbdf4d930b2a67c56572a9788592b943748f6e41c30483728f3cc24732ffa18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897494"
---
# <a name="swbemservicesdeleteasync-method"></a>Método SWbemServices.DeleteAsync

El **método DeleteAsync** del [**objeto SWbemServices**](swbemservices.md) elimina la clase o instancia especificada en la ruta de acceso del objeto. La llamada a **DeleteAsync** se devuelve inmediatamente y los resultados y el estado se devuelven al autor de la llamada a través de eventos entregados al receptor que se especifica en *objWbemSink*. Para obtener más información sobre cómo crear un receptor, vea [Recibir un evento WMI](receiving-a-wmi-event.md). Solo puede eliminar objetos del espacio de nombres al que está conectado.

Si un proveedor dinámico proporciona la clase o instancia, a veces no es posible eliminar este objeto a menos que el proveedor admita la eliminación de clases o instancias.

Se llama al método en modo asincrónico. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemServices.DeleteAsync( _
  [ ByVal ObjWbemSink ], _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ObjWbemSink* \[ Opcional\]
</dt> <dd>

Receptor de objetos que recibe los resultados de la eliminación. Cree un [**objeto SWbemSink**](swbemsink.md) para recibir los objetos.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obligatorio. Cadena que contiene la ruta de acceso del objeto que desea eliminar. Para obtener más información, [vea Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Determina si se devuelven actualizaciones de estado. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus** (128 (0x80))


</dt> <dd>

Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus** (0 (0x0))


</dt> <dd>

Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto es indefinido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> <dt>

*objWbemAsyncContext* \[ Opcional\]
</dt> <dd>

Objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que vuelve al receptor del objeto para identificar el origen de la llamada asincrónica original. Use este parámetro si realiza varias llamadas asincrónicas con el mismo receptor de objetos. Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando. Este **objeto SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Para obtener más información, vea [Llamar a un método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor. Si la llamada se realiza correctamente, el receptor del objeto recibe la notificación de la eliminación.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método DeleteAsync,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> <dt>

**wbemErrTransportFailure:** 2147749909 (0x80041015)
</dt> <dd>

Error de red, lo que impide el funcionamiento normal.

</dd> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El nombre de usuario y la contraseña actuales o especificados no son válidos ni están autorizados para realizar la conexión.

</dd> <dt>

**wbemErrNotFound:** 2147749890 (0x80041002)
</dt> <dd>

No se encontró el elemento solicitado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta llamada se devuelve inmediatamente. El estado de la operación de eliminación se devuelve al autor de la llamada a través de una devolución de llamada entregada al receptor especificado en *objWbemSink*. Puede realizar el procesamiento final en la implementación de *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Una devolución de llamada asincrónica permite a un usuario no autenticado proporcionar datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> </dl>

 


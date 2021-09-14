---
description: Recupera instancias de una clase especificada según los criterios especificados por el usuario.
ms.assetid: 631cd749-9a39-4606-9a38-0b4bb5b4b2cd
ms.tgt_platform: multiple
title: Método SWbemServices.InstancesOfAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c518cb38a0ecb221f4fcb0d0e7f9ce6dfc226ba9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073054"
---
# <a name="swbemservicesinstancesofasync-method"></a>Método SWbemServices.InstancesOfAsync

El **método InstancesOfAsync** del objeto [**SWbemServices**](swbemservices.md) recupera instancias de una clase especificada según los criterios especificados por el usuario.

Se llama al método en modo asincrónico. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener la explicación de la sintaxis, [consulte Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemServices.InstancesOfAsync( _
  ByVal ObjWbemSink, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ObjWbemSink* 
</dt> <dd>

Receptor de objetos que recibe las instancias de forma asincrónica. Cree un [**objeto SWbemSink**](swbemsink.md) para recibir los objetos.

</dd> <dt>

*strClass* 
</dt> <dd>

Necesario. Cadena que contiene el nombre de la clase para las instancias que desea. Este parámetro no puede estar en blanco.

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Determina la profundidad de la enumeración de llamadas y si la llamada se devuelve inmediatamente. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow** (1 (0x1))


</dt> <dd>

Fuerza a la enumeración a incluir solo subclases inmediatas de la clase primaria especificada.

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep** (0 (0x0))


</dt> <dd>

Valor predeterminado para este parámetro. Este valor obliga a la enumeración a incluir todas las clases de la jerarquía.

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus** (128 (0x80))


</dt> <dd>

Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus** (0 (0x0))


</dt> <dd>

Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Hace que WMI devuelva datos de modificación de clase con la definición de clase base. Para obtener más información, vea [Localizing WMI Class Information](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto es indefinido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera información de contexto debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> <dt>

*objWbemAsyncContext* \[ Opcional\]
</dt> <dd>

Objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que vuelve al receptor del objeto para identificar el origen de la llamada asincrónica original. Use este parámetro si realiza varias llamadas asincrónicas con el mismo receptor de objetos. Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando. Este **objeto SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor. Si se realiza correctamente, el receptor recibe un [**evento OnObjectReady**](swbemsink-onobjectready.md) por instancia. Después de la última instancia, el receptor del objeto recibe [**un evento OnCompleted.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método InstancesOfAsync,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El usuario actual no tiene permiso para ver las instancias de la clase especificada.

</dd> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidClass:** 2147749904 (0x80041010)
</dt> <dd>

La clase especificada no es válida.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Un parámetro especificado no es válido.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta llamada se devuelve inmediatamente. Los objetos y el estado solicitados se devuelven al autor de la llamada a través de devoluciones de llamada entregadas al receptor especificado en *objWbemSink*. Para procesar cada objeto cuando vuelva, cree *un objeto objWbemSink*. [**Subrutina de eventos OnObjectReady.**](swbemsink-onobjectready.md) Una vez devueltos todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Una devolución de llamada asincrónica permite a un usuario no autenticado proporcionar datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, consulte [Establecimiento de la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)

El **método InstancesOfAsync** solo funciona con objetos de clase. No es un error que el enumerador devuelto tenga cero (0) elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 


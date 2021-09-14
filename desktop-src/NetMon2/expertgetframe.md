---
description: Devuelve el fotograma solicitado de una captura cargada.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: Función ExpertGetFrame (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069348"
---
# <a name="expertgetframe-function"></a>Función ExpertGetFrame

La **función ExpertGetFrame** devuelve el fotograma solicitado de una captura cargada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hExpertKey* \[ En\]
</dt> <dd>

Identificador experto único. Monitor de red pasa el identificador *hExpertKey* al experto cuando llama a la [**función Run.**](run.md)

</dd> <dt>

*Dirección* \[ En\]
</dt> <dd>

Valor que identifica cómo Monitor de red busca el marco.



| Value                                                                                                                                                                                         | Significado                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <dt>**GET \_ SPECIFIED \_ FRAME**</dt> </dl>              | Devuelve el marco solicitado.<br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <dt>**GET \_ FRAME \_ NEXT \_ FORWARD**</dt> </dl>    | Devuelve el fotograma siguiente.<br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <dt>**GET \_ FRAME \_ NEXT \_ BACKWARD**</dt> </dl> | Devuelve el marco anterior.<br/>  |



 

</dd> <dt>

*RequestFlags* \[ En\]
</dt> <dd>

Marcas que especifican cómo Monitor de red controlar la solicitud. Especifique una o varias de las marcas siguientes.



| Value                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <dt>**MARCAS \_ APLAZAR AL \_ FILTRO DE INTERFAZ DE \_ \_ USUARIO**</dt> </dl> | Antes de aplicar el parámetro de filtro de presentación del experto que se especifica en *hFilter,* aplique el filtro de pantalla que Monitor de red usa cuando se inicia el experto.<br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <dt>**PROPIEDADES DE \_ ASOCIACIÓN DE \_ MARCAS**</dt> </dl>      | Las propiedades que encuentran todos los analizadores de protocolo con las secciones reclamadas de este marco se adjuntan al marco. Si no se establece la marca, el campo **lpPropertyTable** de la estructura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) (devuelto por **pEFrameDescriptor)** se establecerá en **NULL.**<br/> |



 

</dd> <dt>

*RequestedFrameNumber* \[ En\]
</dt> <dd>

Número del marco solicitado.

</dd> <dt>

*hFilter* \[ En\]
</dt> <dd>

Identificador del filtro de visualización experto. Si el experto no tiene un filtro de visualización, establezca el parámetro en **NULL.**

</dd> <dt>

*pEFrameDescriptor* \[ out\]
</dt> <dd>

Estructura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) que, a la vuelta, describe el marco. El experto debe asignar y liberar la memoria que usa esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto indica el motivo del error. Si el valor devuelto es NMERR EXPERT TERMINATE, el experto debe limpiar y devolver inmediatamente; el usuario ha \_ \_ anulado la ejecución del experto.

## <a name="remarks"></a>Observaciones

Si establece FLAGS ATTACH PROPERTIES, la llamada requiere más recursos \_ que si no establece la \_ marca. Si no se establece la marca, un puntero apunta al marco sin formato y a los datos sobre el marco. Si se establece esta marca, Monitor de red todas las propiedades al marco llamando a todos los analizadores que reclaman una parte del marco. Puede ser un proceso lento.

Los expertos no deben establecer la marca FLAGS ATTACH PROPERTIES a menos que los expertos requieran las propiedades que los \_ \_ analizadores adjuntan al marco. Si es posible, los expertos deben llamar a la **función ExpertGetFrame** sin la marca y, a continuación, extraer los datos necesarios directamente del marco.

Si el experto llama a **ExpertGetFrame** sin la marca FLAGS ATTACH PROPERTIES y requiere las propiedades asociadas a ese marco (por ejemplo, un evento), el experto llama a \_ \_ **ExpertGetFrame** con los mismos parámetros, excepto lo siguiente:

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

El uso del código anterior garantiza que el experto obtiene el marco necesario sin tener que volver a llamar al código de filtro.

Puede establecer el *parámetro hFilter* como **LPVOID.** Si existe, el marco devuelto pasa este filtro. Si el experto no tiene un filtro de visualización para pasar a la función (si *hFilter* es **NULL),** el marco devuelto no se filtra.

La **función ExpertGetFrame** solo puede ser llamada por expertos que implementan la función de exportación [**Ejecutar**](run.md) [**o**](configure.md) configurar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





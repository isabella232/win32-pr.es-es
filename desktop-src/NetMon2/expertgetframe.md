---
description: Devuelve el marco solicitado desde una captura cargada.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: Función ExpertGetFrame (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907676"
---
# <a name="expertgetframe-function"></a>ExpertGetFrame función)

La función **ExpertGetFrame** devuelve el fotograma solicitado desde una captura cargada.

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

*hExpertKey* \[ de\]
</dt> <dd>

Identificador de experto único. Monitor de red pasa el identificador *hExpertKey* al experto cuando llama a la función [**Run**](run.md) .

</dd> <dt>

*Dirección* \[ de\]
</dt> <dd>

Valor que identifica cómo Monitor de red busca el marco.



| Value                                                                                                                                                                                         | Significado                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <dt>**OBTENER \_ el \_ marco especificado**</dt> </dl>              | Devuelve el marco solicitado.<br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <dt>**OBTENER \_ fotograma \_ siguiente \_ hacia delante**</dt> </dl>    | Devolver el siguiente fotograma.<br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <dt>**OBTENER \_ fotograma \_ siguiente \_ hacia atrás**</dt> </dl> | Devuelve el fotograma anterior.<br/>  |



 

</dd> <dt>

*RequestFlags* \[ de\]
</dt> <dd>

Marcas que especifican cómo debe administrar Monitor de red la solicitud. Especifique una o varias de las marcas siguientes.



| Value                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <dt>**MARCAS \_ \_ de aplazamiento \_ a \_ filtro de interfaz de usuario**</dt> </dl> | Antes de aplicar el parámetro de filtro para mostrar del experto que se especifica en *hFilter*, aplique el filtro de visualización que monitor de red esté usando cuando se inicie el experto.<br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <dt>**\_propiedades de adjuntar marcas \_**</dt> </dl>      | Las propiedades que todos los analizadores de protocolos encuentran con las secciones reclamadas de este marco se adjuntan al marco. Si no se establece la marca, el campo **lpPropertyTable** de la estructura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) (devuelto por **pEFrameDescriptor**) se establecerá en **null**.<br/> |



 

</dd> <dt>

*RequestedFrameNumber* \[ de\]
</dt> <dd>

Número de la trama solicitada.

</dd> <dt>

*hFilter* \[ de\]
</dt> <dd>

Identificador del filtro de visualización del experto. Si el experto no tiene un filtro de visualización, establezca el parámetro en **null**.

</dd> <dt>

*pEFrameDescriptor* \[ enuncia\]
</dt> <dd>

La estructura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) que, en la devolución, describe el marco. El experto debe asignar y liberar la memoria que usa esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no se realiza correctamente, el valor devuelto indica la razón del error. Si el valor devuelto es NMERR \_ Expert \_ Terminate, el experto debe limpiarse y devolverse inmediatamente; el usuario ha anulado la ejecución del experto.

## <a name="remarks"></a>Observaciones

Si establece \_ las propiedades de adjuntar marcas \_ , la llamada requiere más recursos que si no se establece la marca. Si no se establece la marca, un puntero apunta al fotograma sin formato y a los datos sobre el marco. Si se establece esta marca, Monitor de red asocia todas las propiedades al marco llamando a cada analizador que notifica una parte del marco. Esto puede ser un proceso lento.

Los expertos no deben establecer la \_ marca propiedades de adjuntar marcas a \_ menos que los expertos requieran las propiedades que los analizadores adjuntan al marco. Si es posible, los expertos deben llamar a la función **ExpertGetFrame** sin la marca y, a continuación, extraer los datos necesarios directamente del marco.

Si el experto llama a **ExpertGetFrame** sin el \_ marcador Flags Attach \_ Properties y requiere las propiedades asociadas a ese marco (un evento, por ejemplo), el experto llama a **ExpertGetFrame** con los mismos parámetros, excepto los siguientes:

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

El uso del código anterior garantiza que el experto obtiene el marco necesario sin tener que volver a llamar al código de filtro.

Puede establecer el parámetro *hFilter* como **LPVOID**. Si existe, el fotograma devuelto pasa este filtro. Si el experto no tiene un filtro de visualización para pasar a la función (si *hFilter* es **null** ), el fotograma devuelto no se filtra.

La función **ExpertGetFrame** solo puede ser llamada por expertos que implementan la función de exportación [**Ejecutar**](run.md) o [**configurar**](configure.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





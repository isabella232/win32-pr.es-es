---
description: La función de exportación RecognizeFrame indica si un fragmento de datos se reconoce como el protocolo que detecta el analizador. La función de exportación RecognizeFrame se debe implementar para cada analizador que admita el archivo DLL del analizador.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Función de devolución de llamada RecognizeFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: e2660629cecfa279377794749714102077fb6979
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678515"
---
# <a name="recognizeframe-callback-function"></a>Función de devolución de llamada RecognizeFrame

La función de exportación **RecognizeFrame** indica si un fragmento de datos se reconoce como el protocolo que detecta el analizador. La función de exportación **RecognizeFrame** se debe implementar para cada analizador que admita el archivo DLL del analizador.

## <a name="syntax"></a>Sintaxis


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador del marco que contiene los datos.

</dd> <dt>

*lpFrame* \[ de\]
</dt> <dd>

Puntero al primer byte de un marco. El puntero proporciona una manera de ver los datos que otros analizadores reconocen.

</dd> <dt>

*lpProtocol* \[ de\]
</dt> <dd>

Puntero al inicio de los datos no reclamados. Normalmente, los datos no reclamados se encuentran en medio de un marco porque un analizador anterior ha reclamado los datos antes de este analizador. El analizador debe probar los datos no reclamados en primer lugar.

</dd> <dt>

*MacType* \[ de\]
</dt> <dd>

Valor MAC del primer protocolo en un marco. Normalmente, se usa el valor *MacType* cuando el analizador debe identificar el primer protocolo en un marco. El valor de *MacType* puede ser uno de los siguientes:



| Value                                                                                                                                                                         | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**\_Ethernet de tipo Mac \_**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**\_TOKENRING de tipo Mac \_**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**\_FDDI de tipo Mac \_**</dt> </dl>                | ANSI X3T 9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ de\]
</dt> <dd>

El número restante de bytes desde una ubicación en un marco hasta el final del marco.

</dd> <dt>

*hPreviousProtocol* \[ de\]
</dt> <dd>

Identificador del protocolo anterior.

</dd> <dt>

*nPreviousProtocolOffset* \[ de\]
</dt> <dd>

Desplazamiento del protocolo anterior a partir del marco.

</dd> <dt>

*ProtocolStatusCode* \[ enuncia\]
</dt> <dd>

Indicador de estado del protocolo. El archivo DLL del analizador debe establecer uno de los siguientes códigos de estado.



| Value                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <dt>**Estado de protocolo \_ \_ reconocido**</dt> </dl>              | El analizador reconoce los datos, pero no sabe qué protocolo sigue. Después de establecer el código, devuelva un puntero a los datos restantes no reclamados que siguen el protocolo reconocido. Monitor de red usa el [*siguiente conjunto*](f.md) de protocolos para continuar el análisis. <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <dt>**Estado del protocolo \_ \_ no \_ reconocido**</dt> </dl> | El analizador no reconoce los datos. Después de establecer este código, devuelva el puntero al principio de los datos mediante el puntero que el parámetro *lpProtocol* pasa a la dll del analizador. Monitor de red usa el *siguiente conjunto* del protocolo anterior para continuar el análisis. <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <dt>**Estado de protocolo \_ \_ reclamado**</dt> </dl>                       | El analizador reconoce los datos y notifica el resto de los datos. Después de establecer el código, devuelva **null** para que monitor de red termine de analizar un fotograma. <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <dt>**Protocolo de estado de protocolo \_ \_ siguiente \_**</dt> </dl>    | El analizador reconoce los datos y sabe qué protocolo sigue. Después de establecer el código, establezca el parámetro *phNextProtocol* y devuelva un puntero a los datos restantes no notificados que siguen el protocolo reconocido. Monitor de red continúa analizando el marco. <br/>                               |



 

</dd> <dt>

*phNextProtocol* \[ enuncia\]
</dt> <dd>

Puntero al identificador del protocolo siguiente. Este parámetro se establece cuando un protocolo identifica el protocolo que sigue a un protocolo. Para obtener el identificador del protocolo siguiente, llame a la función [GetProtocolFromTable](getprotocolfromtable.md) .

</dd> <dt>

*lpInstData* \[ in, out\]
</dt> <dd>

En la entrada, un puntero a los datos de instancia del protocolo anterior.

En la salida, puntero a los datos de instancia para el protocolo actual. Los datos de instancia no pueden tener más de una \_ longitud de DWORD PTR.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero al primer byte después de los datos de analizador reconocidos. Si el analizador notifica todos los datos restantes, el valor devuelto es **null**.

Si la función no es correcta, el valor devuelto es un puntero inicial en el que se pasa el parámetro *lpProtocol* .

## <a name="remarks"></a>Observaciones

La función **RecognizeFrame** determina si el analizador reconoce los datos sin procesar a partir del puntero *lpProtocol* .

-   Si el protocolo reconoce los datos, la función **RecognizeFrame** devuelve un puntero a los datos restantes o devuelve **null** si el protocolo actual es el último protocolo de un marco.
-   Si el Protocolo no reconoce los datos, la función **RecognizeFrame** devuelve el puntero que se pasa a la dll del analizador en el parámetro *lpProtocol* .

> [!Note]  
> Se puede llamar a *RecognizeFrame* antes de llamar a la función [*Register*](register-parser.md) para registrar las propiedades del protocolo. Por ese motivo, la implementación de la función *RecognizeFrame* no se basa en las propiedades o estructuras que se crean o inicializan durante la implementación de la función de **registro** de protocolo.

 

**Conjunto de entrega y seguimiento del conjunto**

Un analizador puede usar un conjunto de entrega o un conjunto de seguimiento para identificar Monitor de red el protocolo que sigue a los datos reconocidos.

-   Si la información está disponible en los datos reconocidos, el analizador utiliza su conjunto de entrega para obtener un identificador para el siguiente protocolo y, a continuación, pasa ese identificador a Monitor de red.
-   Si la información no está disponible, el analizador no pasa un identificador y Monitor de red usa el siguiente conjunto de análisis para determinar qué protocolo sigue.

**Pasar información entre protocolos**

Use el parámetro *lpInstData* para pasar información entre protocolos. En la entrada, puede recuperar la información del protocolo anterior. En la salida, puede pasar información al siguiente protocolo.

Los datos de instancia pueden ser cualquier dato que sea menor o igual que \_ la longitud de un valor DWORD PTR, o un puntero a los datos, como los datos de fotogramas sin formato, que no es necesario que el analizador asigne o libere.



| Para obtener información sobre                                        | Vea                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                                                                                    |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.        | [Arquitectura de DLL de analizador](parser-dll-architecture.md)                                                                    |
| Cómo implementar **RecognizeFrame**  incluye un ejemplo. | [Implementación de RecognizeFrame](implementing-recognizeframe.md)                                                            |
| Cómo especificar un conjunto de entrega y seguir el conjunto.              | [Especificar un conjunto de entrega](specifying-a-handoff-set.md)que[Especifique un conjunto de seguimiento](specifying-a-follow-set.md)<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> </dl>

 

 





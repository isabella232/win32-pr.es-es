---
description: La función de exportación RecognizeFrame indica si un fragmento de datos se reconoce como el protocolo que detecta el analizador. La función de exportación RecognizeFrame debe implementarse para cada analizador que admita el archivo DLL del analizador.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Función de devolución de llamada RecognizeFrame (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362119"
---
# <a name="recognizeframe-callback-function"></a>Función de devolución de llamada RecognizeFrame

La **función de exportación RecognizeFrame** indica si un fragmento de datos se reconoce como el protocolo que detecta el analizador. La **función de exportación RecognizeFrame** debe implementarse para cada analizador que admita el archivo DLL del analizador.

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

*hFrame* \[ En\]
</dt> <dd>

Controle el marco que contiene los datos.

</dd> <dt>

*lpFrame* \[ En\]
</dt> <dd>

Puntero al primer byte de un marco. El puntero proporciona una manera de ver los datos que otros analizadores reconocen.

</dd> <dt>

*lpProtocol* \[ En\]
</dt> <dd>

Puntero al inicio de los datos no reclamados. Normalmente, los datos no reclamados se encuentran en medio de un marco porque un analizador anterior ha reclamado datos antes que este analizador. El analizador debe probar primero los datos no reclamados.

</dd> <dt>

*MacType* \[ En\]
</dt> <dd>

Valor MAC del primer protocolo en un marco. Normalmente, el *valor MacType* se usa cuando el analizador debe identificar el primer protocolo de un marco. El *valor macType* puede ser uno de los siguientes:



| Value                                                                                                                                                                         | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**ETHERNET \_ DE TIPO \_ MAC**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**TOKENRING \_ DE \_ TIPO MAC**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**FDDI \_ DE TIPO \_ MAC**</dt> </dl>                | ANSI X3T9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ En\]
</dt> <dd>

Número restante de bytes desde una ubicación de un marco hasta el final del marco.

</dd> <dt>

*hPreviousProtocol* \[ En\]
</dt> <dd>

Identificador del protocolo anterior.

</dd> <dt>

*nPreviousProtocolOffset* \[ En\]
</dt> <dd>

Desplazamiento del principio del protocolo anterior del marco.

</dd> <dt>

*ProtocolStatusCode* \[ out\]
</dt> <dd>

Indicador de estado del protocolo. El archivo DLL del analizador debe establecer uno de los siguientes códigos de estado.



| Value                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <dt>**ESTADO \_ DE \_ PROTOCOLO RECONOCIDO**</dt> </dl>              | El analizador reconoce los datos, pero no sabe qué protocolo sigue. Después de establecer el código, devuelva un puntero a los datos no reclamados restantes que siguen el protocolo reconocido. Monitor de red el siguiente [*conjunto*](f.md) del protocolo para continuar el análisis. <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <dt>**ESTADO \_ DEL PROTOCOLO NO \_ \_ RECONOCIDO**</dt> </dl> | El analizador no reconoce los datos. Después de establecer este código, devuelva el puntero al principio de los datos mediante el puntero que el parámetro *lpProtocol* pasa al archivo DLL del analizador. Monitor de red el siguiente *conjunto* del protocolo anterior para continuar el análisis. <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <dt>**ESTADO \_ DE PROTOCOLO \_ RECLAMADO**</dt> </dl>                       | El analizador reconoce los datos y reclama los datos restantes. Después de establecer el código, devuelva **NULL** para Monitor de red finalizar el análisis de un marco. <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <dt>**PROTOCOLO DE \_ ESTADO DE PROTOCOLO SIGUIENTE \_ \_ PROTOCOLO**</dt> </dl>    | El analizador reconoce los datos y sabe qué protocolo sigue. Después de establecer el código, establezca el parámetro *phNextProtocol* y devuelva un puntero a los datos no reclamados restantes que siguen el protocolo reconocido. Monitor de red continúa analizando el marco. <br/>                               |



 

</dd> <dt>

*phNextProtocol* \[ out\]
</dt> <dd>

Puntero al identificador del protocolo siguiente. Este parámetro se establece cuando un protocolo identifica el protocolo que sigue a un protocolo. Para obtener el identificador del protocolo siguiente, llame a la [función GetProtocolFromTable.](getprotocolfromtable.md)

</dd> <dt>

*lpInstData* \[ in, out\]
</dt> <dd>

En la entrada, puntero a los datos de instancia del protocolo anterior.

En la salida, puntero a los datos de instancia para el protocolo actual. Los datos de instancia no pueden tener una longitud superior a \_ DWORD PTR.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero al primer byte después de los datos del analizador reconocidos. Si el analizador solicita todos los datos restantes, el valor devuelto es **NULL.**

Si la función no se realiza correctamente, el valor devuelto es un puntero inicial que pasa el parámetro *lpProtocol.*

## <a name="remarks"></a>Observaciones

La **función RecognizeFrame** determina si el analizador reconoce los datos sin procesar a partir del *puntero lpProtocol.*

-   Si el protocolo reconoce los datos, la función **RecognizeFrame** devuelve un puntero a los datos restantes o devuelve **NULL** si el protocolo actual es el último protocolo de un marco.
-   Si el protocolo no reconoce los datos, la función **RecognizeFrame** devuelve el puntero pasado al archivo DLL del analizador en el *parámetro lpProtocol.*

> [!Note]  
> *Se puede llamar* a RecognizeFrame antes de [*llamar a la función Register*](register-parser.md) para registrar las propiedades del protocolo. Por ese motivo, la implementación de la función *RecognizeFrame* no se basa en ninguna propiedad o estructura que se cree o inicialice durante la implementación de la función **Register del** protocolo.

 

**Conjunto de entrega y seguimiento del conjunto**

Un analizador puede usar un conjunto de entrega o un conjunto de seguimiento para identificar para Monitor de red protocolo que sigue a los datos reconocidos.

-   Si la información está disponible en datos reconocidos, el analizador usa su conjunto de entregas para obtener un identificador para el protocolo siguiente y, a continuación, pasa ese identificador a Monitor de red.
-   Si la información no está disponible, el analizador no pasa un identificador y Monitor de red el conjunto de seguimiento del analizador para determinar qué protocolo sigue.

**Pasar información entre protocolos**

Use el *parámetro lpInstData* para pasar información entre protocolos. En la entrada, puede recuperar la información del protocolo anterior. En la salida, puede pasar información al protocolo siguiente.

Los datos de instancia pueden ser datos menores o iguales que un PTR DWORD de longitud, o un puntero a datos, como datos de fotogramas sin procesar, que el analizador no necesita asignar o \_ liberar.



| Para obtener información sobre                                        | Vea                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                                                                                    |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.        | [Arquitectura dll del analizador](parser-dll-architecture.md)                                                                    |
| La implementación de **RecognizeFrame**  incluye un ejemplo. | [Implementación de RecognizeFrame](implementing-recognizeframe.md)                                                            |
| Cómo especificar un conjunto de entrega y seguir el conjunto.              | [Especificar un conjunto de entrega especificando](specifying-a-handoff-set.md)[un conjunto siguiente](specifying-a-follow-set.md)<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> </dl>

 

 





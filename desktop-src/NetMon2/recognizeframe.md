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
# <a name="recognizeframe-callback-function"></a><span data-ttu-id="4bdcd-104">Función de devolución de llamada RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="4bdcd-104">RecognizeFrame callback function</span></span>

<span data-ttu-id="4bdcd-105">La función de exportación **RecognizeFrame** indica si un fragmento de datos se reconoce como el protocolo que detecta el analizador.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-105">The **RecognizeFrame** export function indicates whether a piece of data is recognized as the protocol that the parser detects.</span></span> <span data-ttu-id="4bdcd-106">La función de exportación **RecognizeFrame** se debe implementar para cada analizador que admita el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-106">The **RecognizeFrame** export function must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bdcd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bdcd-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4bdcd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bdcd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bdcd-109">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bdcd-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdcd-110">Identificador del marco que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-110">Handle to the frame that contains the data.</span></span>

</dd> <dt>

<span data-ttu-id="4bdcd-111">*lpFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bdcd-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdcd-112">Puntero al primer byte de un marco.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-112">Pointer to the first byte of a frame.</span></span> <span data-ttu-id="4bdcd-113">El puntero proporciona una manera de ver los datos que otros analizadores reconocen.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-113">The pointer provides a way to view data that other parsers recognize.</span></span>

</dd> <dt>

<span data-ttu-id="4bdcd-114">*lpProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bdcd-114">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdcd-115">Puntero al inicio de los datos no reclamados.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-115">Pointer to the start of the unclaimed data.</span></span> <span data-ttu-id="4bdcd-116">Normalmente, los datos no reclamados se encuentran en medio de un marco porque un analizador anterior ha reclamado los datos antes de este analizador.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-116">Typically, the unclaimed data is located in the middle of a frame because a previous parser has claimed data before this parser.</span></span> <span data-ttu-id="4bdcd-117">El analizador debe probar los datos no reclamados en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-117">The parser must test the unclaimed data first.</span></span>

</dd> <dt>

<span data-ttu-id="4bdcd-118">*MacType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bdcd-118">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdcd-119">Valor MAC del primer protocolo en un marco.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-119">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="4bdcd-120">Normalmente, se usa el valor *MacType* cuando el analizador debe identificar el primer protocolo en un marco.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-120">Typically, the *MacType* value is used when the parser must identify the first protocol in a frame.</span></span> <span data-ttu-id="4bdcd-121">El valor de *MacType* puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4bdcd-121">The *MacType* value can be one of the following:</span></span>



| <span data-ttu-id="4bdcd-122">Value</span><span class="sxs-lookup"><span data-stu-id="4bdcd-122">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="4bdcd-123">Significado</span><span class="sxs-lookup"><span data-stu-id="4bdcd-123">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="4bdcd-124"><dt>**\_Ethernet de tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdcd-124"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="4bdcd-125">802.3</span><span class="sxs-lookup"><span data-stu-id="4bdcd-125">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="4bdcd-126"><dt>**\_TOKENRING de tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdcd-126"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="4bdcd-127">802.5</span><span class="sxs-lookup"><span data-stu-id="4bdcd-127">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="4bdcd-128"><dt>**\_FDDI de tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdcd-128"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="4bdcd-129">ANSI X3T 9.5</span><span class="sxs-lookup"><span data-stu-id="4bdcd-129">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="4bdcd-130">*BytesLeft* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bdcd-130">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdcd-131">El número restante de bytes desde una ubicación en un marco hasta el final del marco.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-131">The remaining number of bytes from a location in a frame to the end of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="4bdcd-132">*hPreviousProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bdcd-132">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdcd-133">Identificador del protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-133">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="4bdcd-134">*nPreviousProtocolOffset* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bdcd-134">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdcd-135">Desplazamiento del protocolo anterior a partir del marco.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-135">Offset of the previous protocol   beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="4bdcd-136">*ProtocolStatusCode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4bdcd-136">*ProtocolStatusCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdcd-137">Indicador de estado del protocolo.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-137">Protocol status indicator.</span></span> <span data-ttu-id="4bdcd-138">El archivo DLL del analizador debe establecer uno de los siguientes códigos de estado.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-138">The parser DLL must set one of the following status codes.</span></span>



| <span data-ttu-id="4bdcd-139">Value</span><span class="sxs-lookup"><span data-stu-id="4bdcd-139">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="4bdcd-140">Significado</span><span class="sxs-lookup"><span data-stu-id="4bdcd-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <span data-ttu-id="4bdcd-141"><dt>**Estado de protocolo \_ \_ reconocido**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdcd-141"><dt>**PROTOCOL\_STATUS\_RECOGNIZED**</dt></span></span> </dl>              | <span data-ttu-id="4bdcd-142">El analizador reconoce los datos, pero no sabe qué protocolo sigue.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-142">The parser recognizes the data but does not know which protocol follows.</span></span> <span data-ttu-id="4bdcd-143">Después de establecer el código, devuelva un puntero a los datos restantes no reclamados que siguen el protocolo reconocido.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-143">After setting the code, return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="4bdcd-144">Monitor de red usa el [*siguiente conjunto*](f.md) de protocolos para continuar el análisis.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-144">Network Monitor uses the [*follow set*](f.md) of the protocol to continue parsing.</span></span> <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <span data-ttu-id="4bdcd-145"><dt>**Estado del protocolo \_ \_ no \_ reconocido**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdcd-145"><dt>**PROTOCOL\_STATUS\_NOT\_RECOGNIZED**</dt></span></span> </dl> | <span data-ttu-id="4bdcd-146">El analizador no reconoce los datos.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-146">The parser does not recognize the data.</span></span> <span data-ttu-id="4bdcd-147">Después de establecer este código, devuelva el puntero al principio de los datos mediante el puntero que el parámetro *lpProtocol* pasa a la dll del analizador.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-147">After setting this code, return the pointer to the beginning of the data   using the pointer that the *lpProtocol* parameter passes to the parser DLL.</span></span> <span data-ttu-id="4bdcd-148">Monitor de red usa el *siguiente conjunto* del protocolo anterior para continuar el análisis.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-148">Network Monitor uses the *follow set* of the previous protocol to continue parsing.</span></span> <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <span data-ttu-id="4bdcd-149"><dt>**Estado de protocolo \_ \_ reclamado**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdcd-149"><dt>**PROTOCOL\_STATUS\_CLAIMED**</dt></span></span> </dl>                       | <span data-ttu-id="4bdcd-150">El analizador reconoce los datos y notifica el resto de los datos.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-150">The parser recognizes the data and claims the remaining data.</span></span> <span data-ttu-id="4bdcd-151">Después de establecer el código, devuelva **null** para que monitor de red termine de analizar un fotograma.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-151">After setting the code, return **NULL** for Network Monitor to terminate parsing a frame.</span></span> <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <span data-ttu-id="4bdcd-152"><dt>**Protocolo de estado de protocolo \_ \_ siguiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdcd-152"><dt>**PROTOCOL\_STATUS\_NEXT\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="4bdcd-153">El analizador reconoce los datos y sabe qué protocolo sigue.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-153">The parser recognizes the data and knows which protocol follows.</span></span> <span data-ttu-id="4bdcd-154">Después de establecer el código, establezca el parámetro *phNextProtocol* y devuelva un puntero a los datos restantes no notificados que siguen el protocolo reconocido.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-154">After setting the code, set the *phNextProtocol* parameter, and return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="4bdcd-155">Monitor de red continúa analizando el marco.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-155">Network Monitor continues parsing the frame.</span></span> <br/>                               |



 

</dd> <dt>

<span data-ttu-id="4bdcd-156">*phNextProtocol* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4bdcd-156">*phNextProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdcd-157">Puntero al identificador del protocolo siguiente.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-157">Pointer to the handle of the next protocol.</span></span> <span data-ttu-id="4bdcd-158">Este parámetro se establece cuando un protocolo identifica el protocolo que sigue a un protocolo.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-158">This parameter is set when a protocol identifies the protocol that follows a protocol.</span></span> <span data-ttu-id="4bdcd-159">Para obtener el identificador del protocolo siguiente, llame a la función [GetProtocolFromTable](getprotocolfromtable.md) .</span><span class="sxs-lookup"><span data-stu-id="4bdcd-159">To obtain the handle of the next protocol, call the [GetProtocolFromTable](getprotocolfromtable.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4bdcd-160">*lpInstData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4bdcd-160">*lpInstData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdcd-161">En la entrada, un puntero a los datos de instancia del protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-161">On input, a pointer to the instance data from the previous protocol.</span></span>

<span data-ttu-id="4bdcd-162">En la salida, puntero a los datos de instancia para el protocolo actual.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-162">On output, a pointer to the instance data for the current protocol.</span></span> <span data-ttu-id="4bdcd-163">Los datos de instancia no pueden tener más de una \_ longitud de DWORD PTR.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-163">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bdcd-164">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bdcd-164">Return value</span></span>

<span data-ttu-id="4bdcd-165">Si la función se realiza correctamente, el valor devuelto es un puntero al primer byte después de los datos de analizador reconocidos.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-165">If the function is successful, the return value is a pointer to the first byte after the recognized parser data.</span></span> <span data-ttu-id="4bdcd-166">Si el analizador notifica todos los datos restantes, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-166">If the parser claims all the remaining data, the return value is **NULL**.</span></span>

<span data-ttu-id="4bdcd-167">Si la función no es correcta, el valor devuelto es un puntero inicial en el que se pasa el parámetro *lpProtocol* .</span><span class="sxs-lookup"><span data-stu-id="4bdcd-167">If the function is unsuccessful, the return value is an initial pointer that the *lpProtocol* parameter passes-in.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bdcd-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bdcd-168">Remarks</span></span>

<span data-ttu-id="4bdcd-169">La función **RecognizeFrame** determina si el analizador reconoce los datos sin procesar a partir del puntero *lpProtocol* .</span><span class="sxs-lookup"><span data-stu-id="4bdcd-169">The **RecognizeFrame** function determines whether the parser recognizes the raw data   starting at the *lpProtocol* pointer.</span></span>

-   <span data-ttu-id="4bdcd-170">Si el protocolo reconoce los datos, la función **RecognizeFrame** devuelve un puntero a los datos restantes o devuelve **null** si el protocolo actual es el último protocolo de un marco.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-170">If the protocol recognizes the data, the **RecognizeFrame** function returns a pointer to the remaining data, or returns **NULL** if the current protocol is the last protocol in a frame.</span></span>
-   <span data-ttu-id="4bdcd-171">Si el Protocolo no reconoce los datos, la función **RecognizeFrame** devuelve el puntero que se pasa a la dll del analizador en el parámetro *lpProtocol* .</span><span class="sxs-lookup"><span data-stu-id="4bdcd-171">If the protocol does not recognize the data, the **RecognizeFrame** function returns the pointer passed to the parser DLL in the *lpProtocol* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="4bdcd-172">Se puede llamar a *RecognizeFrame* antes de llamar a la función [*Register*](register-parser.md) para registrar las propiedades del protocolo.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-172">*RecognizeFrame* can be called before the [*Register*](register-parser.md) function is called to register the protocol properties.</span></span> <span data-ttu-id="4bdcd-173">Por ese motivo, la implementación de la función *RecognizeFrame* no se basa en las propiedades o estructuras que se crean o inicializan durante la implementación de la función de **registro** de protocolo.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-173">For that reason, the implementation of the *RecognizeFrame* function does not rely on any properties or structures that are created or initialized during the implementation of the protocol **Register** function.</span></span>

 

<span data-ttu-id="4bdcd-174">**Conjunto de entrega y seguimiento del conjunto**</span><span class="sxs-lookup"><span data-stu-id="4bdcd-174">**Handoff Set and Follow Set**</span></span>

<span data-ttu-id="4bdcd-175">Un analizador puede usar un conjunto de entrega o un conjunto de seguimiento para identificar Monitor de red el protocolo que sigue a los datos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-175">A parser can use a handoff set or follow set to identify for Network Monitor the protocol that follows recognized data.</span></span>

-   <span data-ttu-id="4bdcd-176">Si la información está disponible en los datos reconocidos, el analizador utiliza su conjunto de entrega para obtener un identificador para el siguiente protocolo y, a continuación, pasa ese identificador a Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-176">If information is available in recognized data, the parser uses its handoff set to obtain a handle to the next protocol, and then passes that handle to Network Monitor.</span></span>
-   <span data-ttu-id="4bdcd-177">Si la información no está disponible, el analizador no pasa un identificador y Monitor de red usa el siguiente conjunto de análisis para determinar qué protocolo sigue.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-177">If information is not available, the parser does not pass a handle, and Network Monitor uses the parser follow set to determine which protocol follows.</span></span>

<span data-ttu-id="4bdcd-178">**Pasar información entre protocolos**</span><span class="sxs-lookup"><span data-stu-id="4bdcd-178">**Passing information between protocols**</span></span>

<span data-ttu-id="4bdcd-179">Use el parámetro *lpInstData* para pasar información entre protocolos.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-179">Use the *lpInstData* parameter to pass information between protocols.</span></span> <span data-ttu-id="4bdcd-180">En la entrada, puede recuperar la información del protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-180">On input, you can retrieve the information from the previous protocol.</span></span> <span data-ttu-id="4bdcd-181">En la salida, puede pasar información al siguiente protocolo.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-181">On output, you can pass information to the next protocol.</span></span>

<span data-ttu-id="4bdcd-182">Los datos de instancia pueden ser cualquier dato que sea menor o igual que \_ la longitud de un valor DWORD PTR, o un puntero a los datos, como los datos de fotogramas sin formato, que no es necesario que el analizador asigne o libere.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-182">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>



| <span data-ttu-id="4bdcd-183">Para obtener información sobre</span><span class="sxs-lookup"><span data-stu-id="4bdcd-183">For Information on</span></span>                                        | <span data-ttu-id="4bdcd-184">Vea</span><span class="sxs-lookup"><span data-stu-id="4bdcd-184">See</span></span>                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bdcd-185">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-185">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="4bdcd-186">Analizadores</span><span class="sxs-lookup"><span data-stu-id="4bdcd-186">Parsers</span></span>](parsers.md)                                                                                                    |
| <span data-ttu-id="4bdcd-187">Qué puntos de entrada se incluyen en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-187">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="4bdcd-188">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="4bdcd-188">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                                                                    |
| <span data-ttu-id="4bdcd-189">Cómo implementar **RecognizeFrame**  incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-189">How to implement **RecognizeFrame**  includes an example.</span></span> | [<span data-ttu-id="4bdcd-190">Implementación de RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="4bdcd-190">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)                                                            |
| <span data-ttu-id="4bdcd-191">Cómo especificar un conjunto de entrega y seguir el conjunto.</span><span class="sxs-lookup"><span data-stu-id="4bdcd-191">How to specify a handoff set and follow set.</span></span>              | <span data-ttu-id="4bdcd-192">[Especificar un conjunto de entrega](specifying-a-handoff-set.md)que[Especifique un conjunto de seguimiento](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="4bdcd-192">[Specifying a Handoff Set](specifying-a-handoff-set.md)[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4bdcd-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bdcd-193">Requirements</span></span>



| <span data-ttu-id="4bdcd-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bdcd-194">Requirement</span></span> | <span data-ttu-id="4bdcd-195">Value</span><span class="sxs-lookup"><span data-stu-id="4bdcd-195">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4bdcd-196">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bdcd-196">Minimum supported client</span></span><br/> | <span data-ttu-id="4bdcd-197">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4bdcd-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4bdcd-198">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bdcd-198">Minimum supported server</span></span><br/> | <span data-ttu-id="4bdcd-199">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4bdcd-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4bdcd-200">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bdcd-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bdcd-201"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bdcd-201"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bdcd-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bdcd-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bdcd-203">GetProtocolFromTable</span><span class="sxs-lookup"><span data-stu-id="4bdcd-203">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> </dl>

 

 





---
description: Un conjunto de entrega especifica los protocolos que siguen a un protocolo. El analizador utiliza un conjunto de entrega solo cuando el analizador puede identificar el protocolo siguiente a partir de los datos de una instancia de protocolo.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Especificar un conjunto de entrega
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9acb421963bea3ffaa70b6165c6ffceee138e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686996"
---
# <a name="specifying-a-handoff-set"></a><span data-ttu-id="c019f-104">Especificar un conjunto de entrega</span><span class="sxs-lookup"><span data-stu-id="c019f-104">Specifying a Handoff Set</span></span>

<span data-ttu-id="c019f-105">Un conjunto de entrega especifica los protocolos que siguen a un protocolo.</span><span class="sxs-lookup"><span data-stu-id="c019f-105">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="c019f-106">El analizador utiliza un conjunto de entrega solo cuando el analizador puede identificar el protocolo siguiente a partir de los datos de una instancia de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c019f-106">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="c019f-107">Por ejemplo, el protocolo TCP tiene una propiedad de puerto que identifica el protocolo que sigue al protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="c019f-107">For example, the TCP protocol has a port property that identifies the protocol that follows the TCP protocol.</span></span> <span data-ttu-id="c019f-108">Un valor de propiedad de 20 indica que el protocolo siguiente es FTP.</span><span class="sxs-lookup"><span data-stu-id="c019f-108">A property value of 20 indicates that the next protocol is FTP.</span></span> <span data-ttu-id="c019f-109">Un valor de propiedad de 53 indica que el protocolo siguiente es DNS.</span><span class="sxs-lookup"><span data-stu-id="c019f-109">A property value of 53 indicates that the next protocol is DNS.</span></span> <span data-ttu-id="c019f-110">Dado que la propiedad Port identifica el protocolo que se muestra a continuación, el analizador de TCP puede utilizar el conjunto de entrega siguiente para obtener un identificador para el protocolo que especifica la propiedad Port.</span><span class="sxs-lookup"><span data-stu-id="c019f-110">Because the port property identifies the protocol that follows, the TCP parser can use the following handoff set to get a handle for the protocol that the port property specifies.</span></span>

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

<span data-ttu-id="c019f-111">Los conjuntos de entrega se almacenan en el archivo INI del analizador.</span><span class="sxs-lookup"><span data-stu-id="c019f-111">Handoff sets are stored in the parser INI file.</span></span> <span data-ttu-id="c019f-112">Por ejemplo, el conjunto de entrega TCP anterior se encuentra en tcpip.ini archivo.</span><span class="sxs-lookup"><span data-stu-id="c019f-112">For example, the preceding TCP handoff set is located in tcpip.ini file.</span></span> <span data-ttu-id="c019f-113">Tenga en cuenta que si un archivo DLL de analizador admite varios protocolos, cada analizador que use un conjunto de entrega tendrá su propia ubicación en el archivo INI.</span><span class="sxs-lookup"><span data-stu-id="c019f-113">Note that if a parser DLL supports multiple protocols, each parser that uses a handoff set has its own location in the INI file.</span></span>

<span data-ttu-id="c019f-114">La información del conjunto de entrega se especifica durante la implementación de la función [**ParserAutoInstallInfo**](parserautoinstallinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c019f-114">Handoff set information is specified during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="c019f-115">El analizador puede especificar los protocolos que preceden al protocolo del analizador y los protocolos que siguen el protocolo del analizador.</span><span class="sxs-lookup"><span data-stu-id="c019f-115">The parser can specify the protocols that precede the parser protocol, and the protocols that follow the parser protocol.</span></span> <span data-ttu-id="c019f-116">Monitor de red toma todos los protocolos que preceden y agrega el protocolo del analizador a las siguientes secciones Set del archivo INI del analizador, para cada protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="c019f-116">Network Monitor takes all the protocols that precede, and adds the parser protocol to the follow set sections of the parser INI file — for each preceding protocol.</span></span> <span data-ttu-id="c019f-117">Monitor de red almacena la lista de protocolos que se indican a continuación en la sección conjunto de entrega del archivo INI del analizador.</span><span class="sxs-lookup"><span data-stu-id="c019f-117">Network Monitor stores the list of protocols that follow in the handoff set section of the parser INI file.</span></span>

<span data-ttu-id="c019f-118">Monitor de red almacena la información del conjunto de entrega en el archivo INI del analizador, pero el analizador no accede a los archivos INI directamente.</span><span class="sxs-lookup"><span data-stu-id="c019f-118">Network Monitor stores the handoff set information in the parser INI file, but the parser does not access the INI files directly.</span></span> <span data-ttu-id="c019f-119">Para usar la información del conjunto de entrega, el analizador llama a la función [**CreateHandoffTable**](createhandofftable.md) para crear una tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="c019f-119">To use the information in the handoff set, the parser calls the [**CreateHandoffTable**](createhandofftable.md) function to create a handoff table.</span></span> <span data-ttu-id="c019f-120">Normalmente, la tabla de entrega se crea cuando el analizador registra el protocolo.</span><span class="sxs-lookup"><span data-stu-id="c019f-120">Typically, the handoff table is created when the parser registers the protocol.</span></span> <span data-ttu-id="c019f-121">Una vez registrado el protocolo, Monitor de red crea una tabla de conjunto de entrega que puede usar el analizador.</span><span class="sxs-lookup"><span data-stu-id="c019f-121">After the protocol is registered, Network Monitor creates a handoff set table that the parser can use.</span></span>

<span data-ttu-id="c019f-122">El analizador utiliza su conjunto de entrega al reconocer los datos.</span><span class="sxs-lookup"><span data-stu-id="c019f-122">The parser uses its handoff set when recognizing data.</span></span> <span data-ttu-id="c019f-123">En primer lugar, el analizador lee el valor de la propiedad que identifica el protocolo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c019f-123">First the parser reads the value of the property that identifies the next protocol.</span></span> <span data-ttu-id="c019f-124">A continuación, el analizador llama a [**GetProtocolFromTable**](getprotocolfromtable.md) para obtener un identificador al siguiente protocolo.</span><span class="sxs-lookup"><span data-stu-id="c019f-124">Then the parser calls the [**GetProtocolFromTable**](getprotocolfromtable.md) to get a handle to the next protocol.</span></span> <span data-ttu-id="c019f-125">Por último, el analizador devuelve un puntero al identificador en el parámetro *phNextProtocol* de [**RecognizeFrame**](recognizeframe.md).</span><span class="sxs-lookup"><span data-stu-id="c019f-125">Last, the parser returns a pointer to the handle in the *phNextProtocol* parameter of [**RecognizeFrame**](recognizeframe.md).</span></span>

 

 




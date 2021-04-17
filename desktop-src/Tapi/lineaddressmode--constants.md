---
description: Las \_ constantes de marcador de bits LINEADDRESSMODE describen varias maneras de identificar una dirección en un dispositivo de línea.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: Constantes de LINEADDRESSMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690454"
---
# <a name="lineaddressmode_-constants"></a><span data-ttu-id="13bdb-103">Constantes de LINEADDRESSMODE \_</span><span class="sxs-lookup"><span data-stu-id="13bdb-103">LINEADDRESSMODE\_ Constants</span></span>

<span data-ttu-id="13bdb-104">Las constantes de marcador de bits **LINEADDRESSMODE \_** describen varias maneras de identificar una dirección en un dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="13bdb-104">The **LINEADDRESSMODE\_** bit-flag constants describe various ways of identifying an address on a line device.</span></span>

<dl> <dt>

<span data-ttu-id="13bdb-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ ADDRESSID**</span><span class="sxs-lookup"><span data-stu-id="13bdb-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE\_ADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="13bdb-106">La dirección se especifica con un pequeño entero en el intervalo de 0 a *dwNumAddresses* menos uno, donde *dwNumAddresses* es el valor de las capacidades del dispositivo de la línea.</span><span class="sxs-lookup"><span data-stu-id="13bdb-106">The address is specified with a small integer in the range 0 to *dwNumAddresses* minus one, where *dwNumAddresses* is the value in the line's device capabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="13bdb-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**</span><span class="sxs-lookup"><span data-stu-id="13bdb-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE\_DIALABLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="13bdb-108">La dirección se especifica a través de su número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="13bdb-108">The address is specified through its phone number.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13bdb-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13bdb-109">Remarks</span></span>

<span data-ttu-id="13bdb-110">Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13bdb-110">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="13bdb-111">Los 16 bits de orden inferior están reservados.</span><span class="sxs-lookup"><span data-stu-id="13bdb-111">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="13bdb-112">Esta constante se utiliza para seleccionar una dirección en una línea en la que se origina una llamada.</span><span class="sxs-lookup"><span data-stu-id="13bdb-112">This constant is used to select an address on a line on which to originate a call.</span></span> <span data-ttu-id="13bdb-113">El modelo habitual seleccionaría la dirección por medio de su identificador de dirección.</span><span class="sxs-lookup"><span data-stu-id="13bdb-113">The usual model would select the address by means of its address identifier.</span></span> <span data-ttu-id="13bdb-114">Los identificadores de dirección son el mecanismo que se usa para identificar direcciones en TAPI.</span><span class="sxs-lookup"><span data-stu-id="13bdb-114">Address identifiers are the mechanism used to identify addresses throughout TAPI.</span></span> <span data-ttu-id="13bdb-115">Sin embargo, en algunos entornos, al efectuar una llamada, a menudo es más práctico identificar la dirección de origen de una llamada por el número de teléfono en lugar de por el identificador de dirección.</span><span class="sxs-lookup"><span data-stu-id="13bdb-115">However, in some environments, when making a call, it is often more practical to identify a call's originating address by phone number rather than by address identifier.</span></span> <span data-ttu-id="13bdb-116">Un ejemplo se encuentra en el posible modelado de un gran número de estaciones (de terceros) en el conmutador por medio de un dispositivo de línea con muchas direcciones.</span><span class="sxs-lookup"><span data-stu-id="13bdb-116">One example is in the possible modeling of large numbers of stations (third party) on the switch by means of one line device with many addresses.</span></span> <span data-ttu-id="13bdb-117">La línea representa el conjunto de todas las estaciones y cada estación se asigna a una dirección con su propio número de teléfono principal e identificador de dirección.</span><span class="sxs-lookup"><span data-stu-id="13bdb-117">The line represents the set of all stations, and each station is mapped to an address with its own primary phone number and address identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="13bdb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13bdb-118">Requirements</span></span>



| <span data-ttu-id="13bdb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="13bdb-119">Requirement</span></span> | <span data-ttu-id="13bdb-120">Value</span><span class="sxs-lookup"><span data-stu-id="13bdb-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="13bdb-121">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="13bdb-121">TAPI version</span></span><br/> | <span data-ttu-id="13bdb-122">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="13bdb-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="13bdb-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13bdb-123">Header</span></span><br/>       | <dl> <span data-ttu-id="13bdb-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="13bdb-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 





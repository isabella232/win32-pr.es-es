---
description: En este tema se identifican las constantes que usa WinHTTP.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Constantes WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e37b0e4de7aa3df5e155933bea2be25386c1637
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113175001"
---
# <a name="winhttp-constants"></a><span data-ttu-id="c762e-103">Constantes WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c762e-103">WinHTTP Constants</span></span>

<span data-ttu-id="c762e-104">WinHTTP usa las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="c762e-104">WinHTTP uses the following constants:</span></span>

<dl>

<dt>

[<span data-ttu-id="c762e-105">**mensajes de error**</span><span class="sxs-lookup"><span data-stu-id="c762e-105">**Error Messages**</span></span>](error-messages.md)
</dt> <dd>

<span data-ttu-id="c762e-106">Mensajes de error específicos de las funciones WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c762e-106">Error messages specific to the WinHTTP functions.</span></span> <span data-ttu-id="c762e-107">Estas funciones también devuelven Windows de error cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="c762e-107">These functions also return Windows error messages where appropriate.</span></span> <span data-ttu-id="c762e-108">El valor que corresponde a cada constante es el valor de la constante para las funciones de la interfaz de programación de aplicaciones (API) y los 16 bits inferiores del número de error para el [**objeto WinHttpRequest.**](winhttprequest.md)</span><span class="sxs-lookup"><span data-stu-id="c762e-108">The value that corresponds to each constant is the value of the constant for the application programming interface (API) functions and the lower 16 bits of the error number for the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

</dd> <dt>

[<span data-ttu-id="c762e-109">**Códigos de estado HTTP**</span><span class="sxs-lookup"><span data-stu-id="c762e-109">**HTTP Status Codes**</span></span>](http-status-codes.md)
</dt> <dd>

<span data-ttu-id="c762e-110">Constantes y valores correspondientes que indican códigos de estado HTTP devueltos por los servidores en Internet.</span><span class="sxs-lookup"><span data-stu-id="c762e-110">Constants and corresponding values that indicate HTTP status codes returned by servers on the Internet.</span></span>

</dd> <dt>

[<span data-ttu-id="c762e-111">**Marcas de opción**</span><span class="sxs-lookup"><span data-stu-id="c762e-111">**Option Flags**</span></span>](option-flags.md)
</dt> <dd>

<span data-ttu-id="c762e-112">Marcas de opción compatibles [**con WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) [**y WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="c762e-112">Option flags supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span> <span data-ttu-id="c762e-113">Todas las marcas de opción válidas tienen un valor mayor o igual que WINHTTP FIRST OPTION y menor o \_ \_ igual que WINHTTP LAST \_ \_ OPTION.</span><span class="sxs-lookup"><span data-stu-id="c762e-113">All valid option flags have a value greater than or equal to WINHTTP\_FIRST\_OPTION and less than or equal to WINHTTP\_LAST\_OPTION.</span></span>

</dd> <dt>

[<span data-ttu-id="c762e-114">**PUERTO DE \_ INTERNET**</span><span class="sxs-lookup"><span data-stu-id="c762e-114">**INTERNET\_PORT**</span></span>](internet-port.md)
</dt> <dd>

<span data-ttu-id="c762e-115">Valor de WORD que indica el puerto.</span><span class="sxs-lookup"><span data-stu-id="c762e-115">A WORD value indicating the port.</span></span>

</dd> <dt>

[<span data-ttu-id="c762e-116">**ESQUEMA \_ DE INTERNET**</span><span class="sxs-lookup"><span data-stu-id="c762e-116">**INTERNET\_SCHEME**</span></span>](internet-scheme.md)
</dt> <dd>

<span data-ttu-id="c762e-117">Esquemas de Internet compatibles con WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c762e-117">Internet schemes supported by WinHTTP.</span></span>

</dd>

<dt>

[<span data-ttu-id="c762e-118">**Marcas de información de consulta**</span><span class="sxs-lookup"><span data-stu-id="c762e-118">**Query Info Flags**</span></span>](query-info-flags.md)
</dt>
<dd>

<span data-ttu-id="c762e-119">Atributos y modificadores usados [**por WinHttpQueryHeaders.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)</span><span class="sxs-lookup"><span data-stu-id="c762e-119">Attributes and modifiers used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
</dd>

<dt>

<span data-ttu-id="c762e-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span><span class="sxs-lookup"><span data-stu-id="c762e-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span></span>
</dt>
<dd>

<span data-ttu-id="c762e-121">Tiene un valor de 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c762e-121">Has a value of 0x00000001.</span></span> <span data-ttu-id="c762e-122">Indica a [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) que las cadenas pasadas son cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="c762e-122">Indicates to [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) that the strings passed in are Unicode strings.</span></span>
</dd>

<dt>

<span data-ttu-id="c762e-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span><span class="sxs-lookup"><span data-stu-id="c762e-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span></span>
</dt>
<dd>

<span data-ttu-id="c762e-124">Tiene un valor de 0x00000000000000001ull.</span><span class="sxs-lookup"><span data-stu-id="c762e-124">Has a value of 0x0000000000000001ull.</span></span> <span data-ttu-id="c762e-125">Indica a [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) que no complete la llamada hasta que se haya rellenado el búfer de datos proporcionado o se complete la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c762e-125">Instructs [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) not to complete the call until the provided data buffer has been filled, or the response is complete.</span></span> <span data-ttu-id="c762e-126">Pasar esta marca hace que el comportamiento de **WinHttpReadDataEx** sea equivalente al de [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).</span><span class="sxs-lookup"><span data-stu-id="c762e-126">Passing this flag makes the behavior of **WinHttpReadDataEx** equivalent to that of [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).</span></span>
</dd>

</dl>

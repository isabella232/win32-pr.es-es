---
description: Use tecnologías criptográficas para el cifrado de clave pública, algoritmos de cifrado, cifrado RSA y certificados digitales.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852b7c2b38ca5b7d330a70e91a5b7a9dd5bb6557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666408"
---
# <a name="cryptography"></a><span data-ttu-id="69bd5-103">Criptografía</span><span class="sxs-lookup"><span data-stu-id="69bd5-103">Cryptography</span></span>

## <a name="purpose"></a><span data-ttu-id="69bd5-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="69bd5-104">Purpose</span></span>

<span data-ttu-id="69bd5-105">La criptografía es el uso de códigos para convertir datos de modo que solo un destinatario específico pueda leerlo, mediante una clave.</span><span class="sxs-lookup"><span data-stu-id="69bd5-105">Cryptography is the use of codes to convert data so that only a specific recipient will be able to read it, using a key.</span></span>

<span data-ttu-id="69bd5-106">Las tecnologías de cifrado de Microsoft incluyen CryptoAPI, proveedores de servicios de cifrado (CSP), herramientas de CryptoAPI, CAPICOM, WinTrust, emisión y administración de certificados y desarrollo de infraestructuras de clave pública personalizables.</span><span class="sxs-lookup"><span data-stu-id="69bd5-106">Microsoft cryptographic technologies include CryptoAPI, Cryptographic Service Providers (CSP), CryptoAPI Tools, CAPICOM, WinTrust, issuing and managing certificates, and developing customizable public key infrastructures.</span></span> <span data-ttu-id="69bd5-107">También se describen la inscripción de certificados y tarjetas inteligentes, la administración de certificados y el desarrollo de módulos personalizados.</span><span class="sxs-lookup"><span data-stu-id="69bd5-107">Certificate and smart card enrollment, certificate management, and custom module development are also described.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="69bd5-108">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="69bd5-108">Developer audience</span></span>

<span data-ttu-id="69bd5-109">CryptoAPI está pensado para su uso por parte de desarrolladores de aplicaciones basadas en Windows que permitirán a los usuarios crear e intercambiar documentos y otros datos en un entorno seguro, especialmente en medios no seguros como Internet.</span><span class="sxs-lookup"><span data-stu-id="69bd5-109">CryptoAPI is intended for use by developers of Windows-based applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="69bd5-110">Los desarrolladores deben estar familiarizados con los lenguajes de programación de C y C++ y con el entorno de programación de Windows.</span><span class="sxs-lookup"><span data-stu-id="69bd5-110">Developers should be familiar with the C and C++ programming languages and the Windows programming environment.</span></span> <span data-ttu-id="69bd5-111">Aunque no es necesario, se recomienda comprender los asuntos relacionados con la seguridad o la criptografía.</span><span class="sxs-lookup"><span data-stu-id="69bd5-111">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="69bd5-112">CAPICOM es un componente de solo bits de 32 diseñado para que lo usen los desarrolladores que están creando aplicaciones con el lenguaje de programación de Visual Basic Scripting Edition (VBScript) o el lenguaje de programación C++.</span><span class="sxs-lookup"><span data-stu-id="69bd5-112">CAPICOM is a 32-bit only component that is intended for use by developers who are creating applications using Visual Basic Scripting Edition (VBScript) programming language or the C++ programming language.</span></span> <span data-ttu-id="69bd5-113">CAPICOM está disponible para su uso en los sistemas operativos especificados en Run-Time requisitos.</span><span class="sxs-lookup"><span data-stu-id="69bd5-113">CAPICOM is available for use in the operating systems specified in Run-Time Requirements.</span></span> <span data-ttu-id="69bd5-114">Para un desarrollo futuro, se recomienda usar el .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="69bd5-114">For future development, we recommend that you use the .NET Framework to implement security features.</span></span> <span data-ttu-id="69bd5-115">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).</span><span class="sxs-lookup"><span data-stu-id="69bd5-115">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="69bd5-116">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="69bd5-116">Run-time requirements</span></span>

<span data-ttu-id="69bd5-117">Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="69bd5-117">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="69bd5-118">CAPICOM 2.1.0.2 es compatible con los siguientes sistemas operativos y versiones:</span><span class="sxs-lookup"><span data-stu-id="69bd5-118">CAPICOM 2.1.0.2 is supported on the following operating systems and versions:</span></span>

-   <span data-ttu-id="69bd5-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69bd5-119">Windows Server 2003</span></span>
-   <span data-ttu-id="69bd5-120">Windows XP</span><span class="sxs-lookup"><span data-stu-id="69bd5-120">Windows XP</span></span>

<span data-ttu-id="69bd5-121">CAPICOM está disponible como archivo redistribuible que se puede descargar desde [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span><span class="sxs-lookup"><span data-stu-id="69bd5-121">CAPICOM is available as a redistributable file that can be downloaded from [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span></span>

<span data-ttu-id="69bd5-122">Servicios de Certificate Server requiere las siguientes versiones de estos sistemas operativos:</span><span class="sxs-lookup"><span data-stu-id="69bd5-122">Certificate Services requires the following versions of these operating systems:</span></span>

-   <span data-ttu-id="69bd5-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69bd5-123">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="69bd5-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69bd5-124">Windows Server 2008</span></span>
-   <span data-ttu-id="69bd5-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69bd5-125">Windows Server 2003</span></span>

## <a name="in-this-section"></a><span data-ttu-id="69bd5-126">En esta sección</span><span class="sxs-lookup"><span data-stu-id="69bd5-126">In this section</span></span>



| <span data-ttu-id="69bd5-127">Tema</span><span class="sxs-lookup"><span data-stu-id="69bd5-127">Topic</span></span>                                                           | <span data-ttu-id="69bd5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="69bd5-128">Description</span></span>                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69bd5-129">Acerca de la criptografía</span><span class="sxs-lookup"><span data-stu-id="69bd5-129">About Cryptography</span></span>](about-cryptography.md)<br/>         | <span data-ttu-id="69bd5-130">Conceptos clave de criptografía y una vista de alto nivel de las tecnologías de criptografía de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="69bd5-130">Key cryptography concepts and a high-level view of Microsoft cryptography technologies.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="69bd5-131">Usar criptografía</span><span class="sxs-lookup"><span data-stu-id="69bd5-131">Using Cryptography</span></span>](using-cryptography.md)<br/>         | <span data-ttu-id="69bd5-132">Procesos criptográficos, procedimientos y ejemplos extendidos de C y Visual Basic programas mediante las funciones CryptoAPI y los objetos CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="69bd5-132">Cryptography processes, procedures, and extended samples of C and Visual Basic programs using CryptoAPI functions and CAPICOM objects.</span></span><br/>                                                                            |
| [<span data-ttu-id="69bd5-133">Referencia de criptografía</span><span class="sxs-lookup"><span data-stu-id="69bd5-133">Cryptography Reference</span></span>](cryptography-reference.md)<br/> | <span data-ttu-id="69bd5-134">Descripciones detalladas de las funciones de criptografía de Microsoft, las interfaces, los objetos, las estructuras y otros elementos de programación.</span><span class="sxs-lookup"><span data-stu-id="69bd5-134">Detailed descriptions of the Microsoft cryptography functions, interfaces, objects, structures, and other programming elements.</span></span> <span data-ttu-id="69bd5-135">Incluye descripciones de referencia de la API para trabajar con certificados digitales.</span><span class="sxs-lookup"><span data-stu-id="69bd5-135">Includes reference descriptions of the API for working with digital certificates.</span></span><br/> |



 

 

 





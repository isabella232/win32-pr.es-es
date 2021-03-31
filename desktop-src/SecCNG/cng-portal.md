---
description: CNG es una API de cifrado que se puede usar para crear software de seguridad de cifrado para la administración de claves de cifrado, la criptografía y la seguridad de datos, y la criptografía y la seguridad de red.
ms.assetid: eaad88a1-4e1d-4246-9560-8eef60f8b70f
title: 'Cryptography API: próxima generación'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d485f8371905961c63fbab66b29d0db544e3271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907603"
---
# <a name="cryptography-api-next-generation"></a><span data-ttu-id="2ccd2-103">Cryptography API: próxima generación</span><span class="sxs-lookup"><span data-stu-id="2ccd2-103">Cryptography API: Next Generation</span></span>

## <a name="purpose"></a><span data-ttu-id="2ccd2-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="2ccd2-104">Purpose</span></span>

<span data-ttu-id="2ccd2-105">Cryptography API: Next Generation (CNG) es el sustituto a largo plazo de [*CryptoAPI*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2ccd2-105">Cryptography API: Next Generation (CNG) is the long-term replacement for the [*CryptoAPI*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="2ccd2-106">CNG está diseñado para ser extensible en muchos niveles y en un comportamiento independiente de la criptografía.</span><span class="sxs-lookup"><span data-stu-id="2ccd2-106">CNG is designed to be extensible at many levels and cryptography agnostic in behavior.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2ccd2-107">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="2ccd2-107">Developer audience</span></span>

<span data-ttu-id="2ccd2-108">CNG está diseñado para que lo usen los desarrolladores de aplicaciones que permitirán a los usuarios crear e intercambiar documentos y otros datos en un entorno seguro, especialmente en medios no seguros como Internet.</span><span class="sxs-lookup"><span data-stu-id="2ccd2-108">CNG is intended for use by developers of applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="2ccd2-109">Los desarrolladores deben estar familiarizados con los lenguajes de programación C y C++ y el entorno de programación basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="2ccd2-109">Developers should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="2ccd2-110">Aunque no es necesario, se recomienda comprender los asuntos relacionados con la seguridad o la criptografía.</span><span class="sxs-lookup"><span data-stu-id="2ccd2-110">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="2ccd2-111">Si va a desarrollar un proveedor de algoritmos criptográficos CNG o un proveedor de almacenamiento de claves, debe descargar el [Kit de desarrollo de proveedores de servicios criptográficos](https://www.microsoft.com/download/details.aspx?id=30688) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2ccd2-111">If you are developing a CNG cryptographic algorithm provider or key storage provider, you must download the [Cryptographic Provider Development Kit](https://www.microsoft.com/download/details.aspx?id=30688) from Microsoft.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2ccd2-112">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="2ccd2-112">Run-time requirements</span></span>

<span data-ttu-id="2ccd2-113">CNG se admite a partir de Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2ccd2-113">CNG is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="2ccd2-114">Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="2ccd2-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2ccd2-115">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2ccd2-115">In this section</span></span>



| <span data-ttu-id="2ccd2-116">Tema</span><span class="sxs-lookup"><span data-stu-id="2ccd2-116">Topic</span></span>                                         | <span data-ttu-id="2ccd2-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ccd2-117">Description</span></span>                                                                                                                                    |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ccd2-118">Acerca de CNG</span><span class="sxs-lookup"><span data-stu-id="2ccd2-118">About CNG</span></span>](about-cng.md)<br/>         | <span data-ttu-id="2ccd2-119">Describe las características de CNG, las primitivas criptográficas y el almacenamiento, la recuperación, la importación y la exportación de claves.</span><span class="sxs-lookup"><span data-stu-id="2ccd2-119">Describes CNG features, cryptographic primitives, and key storage, retrieval, import, and export.</span></span><br/>                                   |
| [<span data-ttu-id="2ccd2-120">Usar CNG</span><span class="sxs-lookup"><span data-stu-id="2ccd2-120">Using CNG</span></span>](using-cng.md)<br/>         | <span data-ttu-id="2ccd2-121">Explica cómo usar las características de configuración de criptografía de CNG y la programación de CNG típica.</span><span class="sxs-lookup"><span data-stu-id="2ccd2-121">Explains how to use the cryptography configuration features of CNG and typical CNG programming.</span></span><br/>                                     |
| [<span data-ttu-id="2ccd2-122">Referencia de CNG</span><span class="sxs-lookup"><span data-stu-id="2ccd2-122">CNG Reference</span></span>](cng-reference.md)<br/> | <span data-ttu-id="2ccd2-123">Descripciones detalladas de los elementos de programación de CNG.</span><span class="sxs-lookup"><span data-stu-id="2ccd2-123">Detailed descriptions of the CNG programming elements.</span></span> <span data-ttu-id="2ccd2-124">Estas páginas incluyen descripciones de referencia de la API para trabajar con CNG.</span><span class="sxs-lookup"><span data-stu-id="2ccd2-124">These pages include reference descriptions of the API for working with CNG.</span></span> <br/> |



 

 


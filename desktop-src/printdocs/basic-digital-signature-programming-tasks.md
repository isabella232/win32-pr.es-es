---
description: En esta sección se describe cómo realizar tareas básicas de programación con la API de firma digital XPS.
ms.assetid: a25a8d33-000a-4774-8beb-56d3bb39d5ae
title: Tareas comunes de programación de firmas digitales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346b29c7768f4c4e972284afa697f97bb1da5f69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498106"
---
# <a name="common-digital-signature-programming-tasks"></a><span data-ttu-id="c6869-103">Tareas comunes de programación de firmas digitales</span><span class="sxs-lookup"><span data-stu-id="c6869-103">Common Digital Signature Programming Tasks</span></span>

<span data-ttu-id="c6869-104">En esta sección se describe cómo realizar tareas básicas de programación con la API de firma digital XPS.</span><span class="sxs-lookup"><span data-stu-id="c6869-104">This section describes how to perform basic programming tasks with the XPS Digital Signature API.</span></span>

<span data-ttu-id="c6869-105">Tareas</span><span class="sxs-lookup"><span data-stu-id="c6869-105">Tasks</span></span>

-   [<span data-ttu-id="c6869-106">Inicializar el administrador de firmas</span><span class="sxs-lookup"><span data-stu-id="c6869-106">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)
-   [<span data-ttu-id="c6869-107">Firmar un documento</span><span class="sxs-lookup"><span data-stu-id="c6869-107">Sign a Document</span></span>](sign-a-document.md)
-   [<span data-ttu-id="c6869-108">Agregar una solicitud de firma a un documento XPS</span><span class="sxs-lookup"><span data-stu-id="c6869-108">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
-   [<span data-ttu-id="c6869-109">Comprobar las firmas del documento</span><span class="sxs-lookup"><span data-stu-id="c6869-109">Verify Document Signatures</span></span>](verify-document-signatures.md)

## <a name="disclaimer"></a><span data-ttu-id="c6869-110">Declinación de responsabilidades</span><span class="sxs-lookup"><span data-stu-id="c6869-110">Disclaimer</span></span>

<span data-ttu-id="c6869-111">Los ejemplos de código no pretenden ser completos ni programas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c6869-111">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="c6869-112">Los ejemplos de código a los que se hace referencia en esta página, por ejemplo, no realizan la comprobación de parámetros, la comprobación de errores, la memoria completa o la administración de recursos o el control de errores.</span><span class="sxs-lookup"><span data-stu-id="c6869-112">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, complete memory or resource management, or error handling.</span></span> <span data-ttu-id="c6869-113">Use estos ejemplos como punto de partida y, a continuación, agregue el código necesario para crear una aplicación sólida.</span><span class="sxs-lookup"><span data-stu-id="c6869-113">Use these examples as a starting point, then add the necessary code to create a robust application.</span></span> <span data-ttu-id="c6869-114">Para obtener más información sobre los valores devueltos **HRESULT** y las estrategias de control de errores, vea [control de errores en com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="c6869-114">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="c6869-115">Para mayor claridad, en estos ejemplos de código se usan escenarios de firma y documentos XPS muy sencillos, que podrían no ser suficientemente complejos para satisfacer sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="c6869-115">For clarity, these code examples use very simple XPS document and signature scenarios, which might not be sufficiently complex to meet your needs.</span></span>

 

 

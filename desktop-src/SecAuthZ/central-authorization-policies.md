---
description: Una directiva de autorización central (CAP) recopila las reglas de autorización específicas (CAPRs) en una única directiva.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Directivas de autorización central
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b890236b0dae0f8f8d51254def4e1607cc35894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648243"
---
# <a name="central-authorization-policies"></a><span data-ttu-id="51b2b-103">Directivas de autorización central</span><span class="sxs-lookup"><span data-stu-id="51b2b-103">Central Authorization Policies</span></span>

<span data-ttu-id="51b2b-104">Una directiva de autorización central (CAP) recopila las reglas de autorización específicas (CAPRs) en una única directiva.</span><span class="sxs-lookup"><span data-stu-id="51b2b-104">A Central Authorization Policy (CAP) collects the specific authorization rules (CAPRs) into a single policy.</span></span> <span data-ttu-id="51b2b-105">Para permitir la combinación de las reglas de autorización específicas (CAPRs) en la Directiva de autorización holística de la organización, se puede hacer referencia a CAPRs y aplicarla a un conjunto de recursos.</span><span class="sxs-lookup"><span data-stu-id="51b2b-105">To allow the specific authorization rules (CAPRs) to be combined into the holistic authorization policy of the organization, CAPRs can be referenced together and applied to a set of resources.</span></span> <span data-ttu-id="51b2b-106">Para ello, se recopilan varios (por referencia) en un extremo.</span><span class="sxs-lookup"><span data-stu-id="51b2b-106">This is done by collecting multiple (by reference) into a CAP.</span></span> <span data-ttu-id="51b2b-107">Una vez definido un extremo, los administradores de recursos pueden distribuirlo para aplicar la Directiva de autorización de la organización a los recursos.</span><span class="sxs-lookup"><span data-stu-id="51b2b-107">Once a CAP is defined it can be distributed consumed by resource managers to apply the organizations authorization policy to resources.</span></span>

<span data-ttu-id="51b2b-108">Un extremo tiene los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="51b2b-108">A CAP has the following attributes:</span></span>

-   <span data-ttu-id="51b2b-109">Colección de CAPRs: una lista de referencias a objetos CAPR existentes</span><span class="sxs-lookup"><span data-stu-id="51b2b-109">Collection of CAPRs – a list of references to existing CAPR objects</span></span>
-   <span data-ttu-id="51b2b-110">Un identificador (SID)</span><span class="sxs-lookup"><span data-stu-id="51b2b-110">An identifier (Sid)</span></span>
-   <span data-ttu-id="51b2b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="51b2b-111">Description</span></span>
-   <span data-ttu-id="51b2b-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="51b2b-112">Name</span></span>

<span data-ttu-id="51b2b-113">Un extremo se evalúa durante la evaluación del acceso para los archivos y carpetas en los que un administrador lo habilita.</span><span class="sxs-lookup"><span data-stu-id="51b2b-113">A CAP is evaluated during access evaluation for files and folders on which an administrator enables it.</span></span> <span data-ttu-id="51b2b-114">Durante una llamada a [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , la comprobación de Cap se combina lógicamente con la comprobación de la ACL discrecional; Esto significa que, para obtener acceso a un archivo al que se aplica el límite, un usuario debe tener acceso ambos según el CAP (su CAPRs asociado) y la ACL discrecional del archivo.</span><span class="sxs-lookup"><span data-stu-id="51b2b-114">During an [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) call, the CAP check is logically combined with the discretionary ACL check; this means that in order to obtain access to a file to which the CAP applies, a user needs to have access both according to the CAP (its associated CAPRs) and the discretionary ACL on the file.</span></span>

<span data-ttu-id="51b2b-115">CAP de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="51b2b-115">Example CAP:</span></span>

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a><span data-ttu-id="51b2b-116">Definición de CAP</span><span class="sxs-lookup"><span data-stu-id="51b2b-116">CAP Definition</span></span>

<span data-ttu-id="51b2b-117">Se crea un extremo y se edita en Active Directory mediante una nueva experiencia de usuario en ADAC (o PowerShell) que permite al administrador crear un CAP y especificar un conjunto de CAPRs que componen el límite.</span><span class="sxs-lookup"><span data-stu-id="51b2b-117">A CAP is created and edited in Active Directory using a new UX in ADAC (or PowerShell) that allows the administrator to create a CAP and specify a set of CAPRs that make up the CAP.</span></span>

 

 

---
description: Se pueden usar las siguientes interfaces para inscribir un usuario o un equipo en una jerarquía de certificados.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Interfaces de inscripción de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688629"
---
# <a name="certificate-enrollment-interfaces"></a><span data-ttu-id="77ace-103">Interfaces de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="77ace-103">Certificate Enrollment Interfaces</span></span>

<span data-ttu-id="77ace-104">Se pueden usar las siguientes interfaces para inscribir un usuario o un equipo en una jerarquía de certificados.</span><span class="sxs-lookup"><span data-stu-id="77ace-104">The following interfaces can be used to enroll a user or a computer in a certificate hierarchy.</span></span>



| <span data-ttu-id="77ace-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="77ace-105">Interface</span></span>                                              | <span data-ttu-id="77ace-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="77ace-106">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77ace-107">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="77ace-107">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | <span data-ttu-id="77ace-108">Inscribe un equipo o usuario en una jerarquía de certificados.</span><span class="sxs-lookup"><span data-stu-id="77ace-108">Enrolls a computer or user in a certificate hierarchy.</span></span>                                                                                                                              |
| [<span data-ttu-id="77ace-109">**IX509Enrollment2**</span><span class="sxs-lookup"><span data-stu-id="77ace-109">**IX509Enrollment2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | <span data-ttu-id="77ace-110">Extiende la interfaz [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para habilitar la inicialización desde una plantilla.</span><span class="sxs-lookup"><span data-stu-id="77ace-110">Extends the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to enable initialization from a template.</span></span>                                                                          |
| [<span data-ttu-id="77ace-111">**IX509EnrollmentHelper**</span><span class="sxs-lookup"><span data-stu-id="77ace-111">**IX509EnrollmentHelper**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | <span data-ttu-id="77ace-112">Define métodos que permiten a una aplicación web inscribir un certificado, almacenar credenciales del servidor de directivas en la caché de credenciales y registrar servidores de directivas y servidores de inscripción.</span><span class="sxs-lookup"><span data-stu-id="77ace-112">Defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.</span></span> |
| [<span data-ttu-id="77ace-113">**IX509EnrollmentStatus**</span><span class="sxs-lookup"><span data-stu-id="77ace-113">**IX509EnrollmentStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | <span data-ttu-id="77ace-114">Recupera información detallada del error sobre una transacción de inscripción de certificado.</span><span class="sxs-lookup"><span data-stu-id="77ace-114">Retrieves detailed error information about a certificate enrollment transaction.</span></span>                                                                                                    |
| [<span data-ttu-id="77ace-115">**IX509SCEPEnrollment**</span><span class="sxs-lookup"><span data-stu-id="77ace-115">**IX509SCEPEnrollment**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | <span data-ttu-id="77ace-116">Interfaz de Protocolo simple de inscripción de equipos X. 509</span><span class="sxs-lookup"><span data-stu-id="77ace-116">X.509 Simple Computer Enrollment Protocol Interface</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="77ace-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77ace-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77ace-118">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="77ace-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 





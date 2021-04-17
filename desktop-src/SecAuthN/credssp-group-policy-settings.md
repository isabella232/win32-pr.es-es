---
description: Para que el protocolo de proveedor de compatibilidad para seguridad de credenciales (CredSSP) delegue las credenciales, debe especificar a qué servidores se puede delegar.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: Configuración de directiva de grupo CredSSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652769"
---
# <a name="credssp-group-policy-settings"></a><span data-ttu-id="f3898-103">Configuración de directiva de grupo CredSSP</span><span class="sxs-lookup"><span data-stu-id="f3898-103">CredSSP Group Policy Settings</span></span>

<span data-ttu-id="f3898-104">Para que el [Protocolo de proveedor de compatibilidad para seguridad de credenciales (CredSSP)](credential-security-support-provider.md) delegue las credenciales, debe especificar a qué servidores se puede delegar.</span><span class="sxs-lookup"><span data-stu-id="f3898-104">For [Credential Security Support Provider protocol (CredSSP)](credential-security-support-provider.md) to delegate credentials, you must specify which servers can be delegated to.</span></span> <span data-ttu-id="f3898-105">Para especificar esos servidores, modifique la configuración en el complemento Microsoft Management Console (MMC) del editor de directiva de grupo (GPE).</span><span class="sxs-lookup"><span data-stu-id="f3898-105">To specify those servers, modify settings in the Group Policy Editor (GPE) Microsoft Management Console (MMC) snap-in.</span></span> <span data-ttu-id="f3898-106">La configuración de GPE que controla la delegación se encuentran en **configuración \| del equipo Plantillas administrativas \| delegación de \| credenciales del sistema**.</span><span class="sxs-lookup"><span data-stu-id="f3898-106">The GPE settings that control delegation are under **Computer Configuration \| Administrative Templates \| System \| Credentials Delegation**.</span></span>

> [!Caution]  
> <span data-ttu-id="f3898-107">Esta no es una delegación restringida.</span><span class="sxs-lookup"><span data-stu-id="f3898-107">This is not constrained delegation.</span></span> <span data-ttu-id="f3898-108">CredSSP pasa las credenciales completas del usuario al servidor sin ninguna restricción.</span><span class="sxs-lookup"><span data-stu-id="f3898-108">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="f3898-109">La configuración de directiva de grupo controla la delegación de los siguientes tipos de credenciales.</span><span class="sxs-lookup"><span data-stu-id="f3898-109">Group policy settings control delegation of the following types of credentials.</span></span>



| <span data-ttu-id="f3898-110">Tipo de credenciales</span><span class="sxs-lookup"><span data-stu-id="f3898-110">Credentials Type</span></span>                                                                                                                                 | <span data-ttu-id="f3898-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3898-111">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3898-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Credenciales predeterminadas</span><span class="sxs-lookup"><span data-stu-id="f3898-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Default credentials</span></span><br/> | <span data-ttu-id="f3898-113">Las credenciales obtenidas cuando el usuario inicia sesión por primera vez en Windows.</span><span class="sxs-lookup"><span data-stu-id="f3898-113">The credentials obtained when the user first logs on to Windows.</span></span><br/>                   |
| <span data-ttu-id="f3898-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Nuevas credenciales</span><span class="sxs-lookup"><span data-stu-id="f3898-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Fresh credentials</span></span><br/>         | <span data-ttu-id="f3898-115">Las credenciales que se solicita al usuario al ejecutar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f3898-115">The credentials that the user is prompted for when executing an application.</span></span><br/>       |
| <span data-ttu-id="f3898-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Credenciales guardadas</span><span class="sxs-lookup"><span data-stu-id="f3898-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Saved credentials</span></span><br/>         | <span data-ttu-id="f3898-117">Las credenciales que se guardan con el [Administrador de credenciales](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="f3898-117">The credentials that are saved using [Credential Manager](credential-manager.md).</span></span><br/> |



 

<span data-ttu-id="f3898-118">Para incluir un servidor en la categoría asociado a una configuración de directiva de grupo determinada, agregue el [*nombre de entidad*](/windows/desktop/SecGloss/s-gly) de seguridad de servicio (SPN) de ese servidor a la lista de servidores de esa configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f3898-118">To include a server in the category associated with a particular group policy setting, add the [*Service Principal Name*](/windows/desktop/SecGloss/s-gly) (SPN) of that server to the list of servers for that group policy setting.</span></span> <span data-ttu-id="f3898-119">El SPN puede contener un solo carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="f3898-119">The SPN can contain a single wildcard character.</span></span>

 


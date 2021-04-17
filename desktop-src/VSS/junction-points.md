---
description: En Windows Vista y Windows Server 2008, las ubicaciones predeterminadas para los datos de usuario y los datos del sistema han cambiado.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Puntos de Unión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697006"
---
# <a name="junction-points"></a><span data-ttu-id="f29bb-103">Puntos de Unión</span><span class="sxs-lookup"><span data-stu-id="f29bb-103">Junction Points</span></span>

<span data-ttu-id="f29bb-104">En Windows Vista y Windows Server 2008, las ubicaciones predeterminadas para los datos de usuario y los datos del sistema han cambiado.</span><span class="sxs-lookup"><span data-stu-id="f29bb-104">In Windows Vista and Windows Server 2008, the default locations for user data and system data have changed.</span></span> <span data-ttu-id="f29bb-105">Por ejemplo, los datos de usuario que se almacenaron previamente en el directorio% SystemDrive% \\ Documents and Settings se almacenan ahora en el directorio% SystemDrive% \\ users.</span><span class="sxs-lookup"><span data-stu-id="f29bb-105">For example, user data that was previously stored in the %SystemDrive%\\Documents and Settings directory is now stored in the %SystemDrive%\\Users directory.</span></span> <span data-ttu-id="f29bb-106">Por compatibilidad con versiones anteriores, las ubicaciones anteriores tienen puntos de Unión que apuntan a las nuevas ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="f29bb-106">For backward compatibility, the old locations have junction points that point to the new locations.</span></span> <span data-ttu-id="f29bb-107">Por ejemplo, C: \\ Documents and Settings es ahora un punto de Unión que apunta a C: \\ users.</span><span class="sxs-lookup"><span data-stu-id="f29bb-107">For example, C:\\Documents and Settings is now a junction point that points to C:\\Users.</span></span> <span data-ttu-id="f29bb-108">Las aplicaciones de copia de seguridad deben ser capaces de realizar copias de seguridad y restaurar puntos de Unión.</span><span class="sxs-lookup"><span data-stu-id="f29bb-108">Backup applications must be capable of backing up and restoring junction points.</span></span>

<span data-ttu-id="f29bb-109">Estos puntos de Unión se pueden identificar de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="f29bb-109">These junction points can be identified as follows:</span></span>

-   <span data-ttu-id="f29bb-110">Tienen el atributo de \_ archivo \_ punto de reanálisis \_ , \_ atributo de archivo \_ oculto y \_ conjunto de atributos de archivo del sistema de atributos de archivo \_ .</span><span class="sxs-lookup"><span data-stu-id="f29bb-110">They have the FILE\_ATTRIBUTE\_REPARSE\_POINT, FILE\_ATTRIBUTE\_HIDDEN, and FILE\_ATTRIBUTE\_SYSTEM file attributes set.</span></span>
-   <span data-ttu-id="f29bb-111">También tienen sus listas de control de acceso (ACL) configuradas para denegar el acceso de lectura a todos.</span><span class="sxs-lookup"><span data-stu-id="f29bb-111">They also have their access control lists (ACLs) set to deny read access to everyone.</span></span>

<span data-ttu-id="f29bb-112">Las aplicaciones que llaman a una ruta de acceso específica pueden atravesar estos puntos de unión si tienen los permisos necesarios.</span><span class="sxs-lookup"><span data-stu-id="f29bb-112">Applications that call out a specific path can traverse these junction points if they have the required permissions.</span></span> <span data-ttu-id="f29bb-113">Sin embargo, los intentos de enumerar el contenido de los puntos de Unión producirán errores.</span><span class="sxs-lookup"><span data-stu-id="f29bb-113">However, attempts to enumerate the contents of the junction points will result in failures.</span></span> <span data-ttu-id="f29bb-114">Es importante que las aplicaciones de copia de seguridad no atraviesen estos puntos de unión o intenten hacer una copia de seguridad de los mismos por dos motivos:</span><span class="sxs-lookup"><span data-stu-id="f29bb-114">It is important that backup applications do not traverse these junction points, or attempt to backup data under them, for two reasons:</span></span>

-   <span data-ttu-id="f29bb-115">Si lo hace, la aplicación de copia de seguridad puede hacer una copia de seguridad de los mismos datos más de una vez.</span><span class="sxs-lookup"><span data-stu-id="f29bb-115">Doing so can cause the backup application to back up the same data more than once.</span></span>
-   <span data-ttu-id="f29bb-116">También puede conducir a ciclos (referencias circulares).</span><span class="sxs-lookup"><span data-stu-id="f29bb-116">It can also lead to cycles (circular references).</span></span>

## <a name="per-user-junctions-and-system-junctions"></a><span data-ttu-id="f29bb-117">Uniones de Per-User y uniones del sistema</span><span class="sxs-lookup"><span data-stu-id="f29bb-117">Per-User Junctions and System Junctions</span></span>

<span data-ttu-id="f29bb-118">Los puntos de Unión que se usan para proporcionar la virtualización de archivos y del registro en Windows Vista y Windows Server 2008 se pueden dividir en dos clases: uniones por usuario y uniones del sistema.</span><span class="sxs-lookup"><span data-stu-id="f29bb-118">The junction points that are used to provide file and registry virtualization in Windows Vista and Windows Server 2008 can be divided into two classes: per-user junctions and system junctions.</span></span>

<span data-ttu-id="f29bb-119">Las uniones por usuario se crean dentro de cada perfil de usuario individual para proporcionar compatibilidad con versiones anteriores para las aplicaciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="f29bb-119">Per-user junctions are created inside each individual user's profile to provide backward compatibility for user applications.</span></span> <span data-ttu-id="f29bb-120">El punto de Unión en C: \\ users \\ *nombreDeUsuario* \\ Mis documentos que señala a c: \\ users \\ *nombreDeUsuario* \\ Documents es un ejemplo de una Unión por usuario.</span><span class="sxs-lookup"><span data-stu-id="f29bb-120">The junction point at C:\\Users\\*username*\\My Documents that points to C:\\Users\\*username*\\Documents is an example of a per-user junction.</span></span> <span data-ttu-id="f29bb-121">El servicio de perfil crea las uniones por usuario cuando se crea el perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="f29bb-121">Per-user junctions are created by the Profile service when the user's profile is created.</span></span>

<span data-ttu-id="f29bb-122">Las demás uniones son uniones del sistema que no residen en el directorio users \\ *username* .</span><span class="sxs-lookup"><span data-stu-id="f29bb-122">The other junctions are system junctions that do not reside under the Users\\*username* directory.</span></span> <span data-ttu-id="f29bb-123">Entre los ejemplos de uniones del sistema se incluyen:</span><span class="sxs-lookup"><span data-stu-id="f29bb-123">Examples of system junctions include:</span></span>

-   <span data-ttu-id="f29bb-124">Documentos y configuración</span><span class="sxs-lookup"><span data-stu-id="f29bb-124">Documents and Settings</span></span>
-   <span data-ttu-id="f29bb-125">Uniones dentro de los perfiles de usuario todos los usuarios, públicos y predeterminados</span><span class="sxs-lookup"><span data-stu-id="f29bb-125">Junctions within the All Users, Public, and Default User profiles</span></span>

<span data-ttu-id="f29bb-126">Las uniones del sistema se crean mediante userenv.dll cuando la bienvenida de Windows la invoca (también se conoce como la máquina rápida o mOOBE).</span><span class="sxs-lookup"><span data-stu-id="f29bb-126">System junctions are created by userenv.dll when it is invoked by Windows Welcome (also called the machine out-of-box-experience, or mOOBE).</span></span>

> [!Note]  
> <span data-ttu-id="f29bb-127">Si el usuario cambia el idioma del sistema a un idioma distinto del inglés, los puntos de Unión por usuario y sistema se crearán con nombres localizados.</span><span class="sxs-lookup"><span data-stu-id="f29bb-127">If the user changes the system language to a language other than English, the per-user and system junction points will be created with localized names.</span></span>

 

 

 




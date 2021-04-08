---
title: ADSI y control de cuentas de usuario
description: Windows y Windows Server tienen control de cuentas de usuario, que tiene ramificaciones para aplicaciones que usan interfaces de servicio de Active Directory (ADSI).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36fc88169a8710228a3bf70283aaccd4b4ac42e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078364"
---
# <a name="adsi-and-user-account-control"></a><span data-ttu-id="7192a-103">ADSI y control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="7192a-103">ADSI and User Account Control</span></span>

<span data-ttu-id="7192a-104">Windows y Windows Server tienen [control de cuentas de usuario](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), que tiene ramificaciones para aplicaciones que usan [interfaces de servicio de Active Directory](active-directory-service-interfaces-adsi.md) (ADSI).</span><span class="sxs-lookup"><span data-stu-id="7192a-104">Windows and Windows Server have [User Account Control](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), which has ramifications for applications that use [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="7192a-105">En concreto, estas interfaces se diseñaron para ejecutarse mediante una cuenta de usuario con privilegios de administrador en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="7192a-105">Specifically, these interfaces were designed to be run by a user account with administrator privileges on the local computer.</span></span>

<span data-ttu-id="7192a-106">**Problema**</span><span class="sxs-lookup"><span data-stu-id="7192a-106">**Problem**</span></span>

<span data-ttu-id="7192a-107">Cada vez que una aplicación se conecta al directorio e intenta crear un objeto ADSI, se comprueba si hay cambios en el [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) .</span><span class="sxs-lookup"><span data-stu-id="7192a-107">Every time an application connects to the directory and attempts to create an ADSI object, the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) is checked for changes.</span></span> <span data-ttu-id="7192a-108">Si ha cambiado desde la última conexión, el esquema se descarga y se almacena en una caché del equipo local.</span><span class="sxs-lookup"><span data-stu-id="7192a-108">If it has changed since the last connection, the schema is downloaded and stored in a cache on the local computer.</span></span> <span data-ttu-id="7192a-109">En versiones de Windows anteriores a Windows Vista, la ubicación predeterminada de esta caché era</span><span class="sxs-lookup"><span data-stu-id="7192a-109">In versions of Windows prior to Windows Vista, the default location for this cache was</span></span>

`%systemroot%\SchCache\`

<span data-ttu-id="7192a-110">Sin embargo, las aplicaciones que se ejecutan con cuentas estándar (es decir, sin administrador) no tendrán acceso a este directorio y, por lo tanto, las aplicaciones que usen interfaces ADSI que se ejecuten en este modo descargarán el esquema en cada conexión, lo que afectará al rendimiento y al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7192a-110">However, applications run by standard (that is, non-administrator) accounts will not have access to this directory, and consequently, applications that use ADSI interfaces that are run in this mode will download the schema on every connection, which will impact throughput and performance.</span></span>

<span data-ttu-id="7192a-111">**Soluciones**</span><span class="sxs-lookup"><span data-stu-id="7192a-111">**Solutions**</span></span>

<span data-ttu-id="7192a-112">*Usuario único* : para resolver este problema, hay nuevas claves de control del registro del proveedor ADSI que determinan las ubicaciones del registro y las ubicaciones de los archivos para los objetos de [esquema Active Directory](/windows/desktop/ADSchema/active-directory-schema) almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="7192a-112">*Single user* - To resolve this issue, there are new ADSI Provider registry control keys that determine the registry locations and file locations for cached [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects.</span></span> <span data-ttu-id="7192a-113">Si la clave del registro</span><span class="sxs-lookup"><span data-stu-id="7192a-113">If the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="7192a-114">está establecido en 0 (cero), cada usuario tendrá una ubicación de almacenamiento diferente para ADSI; las claves del registro se almacenarán en</span><span class="sxs-lookup"><span data-stu-id="7192a-114">is set to 0 (zero), each user will have a different storage location for ADSI; registry keys will be stored in</span></span>

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

<span data-ttu-id="7192a-115">y los archivos de caché se almacenarán en</span><span class="sxs-lookup"><span data-stu-id="7192a-115">and cache files will be stored in</span></span>

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

<span data-ttu-id="7192a-116">Esta configuración es la predeterminada en los equipos que ejecutan Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7192a-116">These settings are the default settings on computers running Windows Server 2008 or Windows Vista.</span></span>

<span data-ttu-id="7192a-117">*Multiusuario* : Si está ejecutando aplicaciones ADSI en un equipo con muchas cuentas de usuario (por ejemplo, un servidor Web), es preferible no tener muchas copias de la memoria caché del [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) con grandes cantidades de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="7192a-117">*Multi-user* - If you are running ADSI applications on a computer with many user accounts (for example, a web server), then it's preferable not to have many copies of the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) cache using up large amounts of disk space.</span></span> <span data-ttu-id="7192a-118">Establecimiento de la clave del registro</span><span class="sxs-lookup"><span data-stu-id="7192a-118">Setting the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="7192a-119">a 1 (uno) revertirá ADSI al comportamiento anterior; todos los objetos de [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) se almacenarán en sus ubicaciones anteriores; la clave del registro estará en</span><span class="sxs-lookup"><span data-stu-id="7192a-119">to 1 (one) will revert ADSI to the previous behavior; all [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects will be stored in their previous locations; the registry key will be in</span></span>

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

<span data-ttu-id="7192a-120">y el archivo de caché estará en</span><span class="sxs-lookup"><span data-stu-id="7192a-120">and the cache file will be in</span></span>

`%systemroot%\SchCache`

<span data-ttu-id="7192a-121">En este caso, las cuentas de administrador deben ejecutar la aplicación, lo que hará que el archivo de esquema se almacene en caché en la ubicación global para un uso futuro por parte de los usuarios con menos privilegios.</span><span class="sxs-lookup"><span data-stu-id="7192a-121">In this case, administrator accounts should run the application, which will cause the schema file to be cached in the global location for future use by the less privileged users.</span></span>

 

 
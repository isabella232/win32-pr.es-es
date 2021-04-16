---
description: Usar las funciones de CryptoAPI para administrar almacenes de certificados y certificados, listas de revocación de certificados y listas de certificados de confianza dentro de esas tiendas.
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: Administración de certificados con almacenes de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98abb2b612f77db3f1c59e53fb9c7bf0f34cefb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567288"
---
# <a name="managing-certificates-with-certificate-stores"></a><span data-ttu-id="4018e-103">Administración de certificados con almacenes de certificados</span><span class="sxs-lookup"><span data-stu-id="4018e-103">Managing Certificates with Certificate Stores</span></span>

<span data-ttu-id="4018e-104">Durante un período de tiempo, los [*certificados*](../secgloss/c-gly.md) se acumularán en el equipo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="4018e-104">Over a period of time, [*certificates*](../secgloss/c-gly.md) will accumulate on a user's computer.</span></span> <span data-ttu-id="4018e-105">Las herramientas son necesarias para administrar estos certificados.</span><span class="sxs-lookup"><span data-stu-id="4018e-105">Tools are required to manage these certificates.</span></span> <span data-ttu-id="4018e-106">[*CryptoAPI*](../secgloss/c-gly.md) proporciona esas herramientas como funciones para almacenar, recuperar, eliminar, enumerar (enumerar) y comprobar los certificados.</span><span class="sxs-lookup"><span data-stu-id="4018e-106">[*CryptoAPI*](../secgloss/c-gly.md) provides those tools as functions to store, retrieve, delete, list (enumerate), and verify certificates.</span></span> <span data-ttu-id="4018e-107">CryptoAPI también proporciona los medios para adjuntar certificados a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="4018e-107">CryptoAPI also provides the means to attach certificates to messages.</span></span>

<span data-ttu-id="4018e-108">CryptoAPI ofrece dos categorías principales de funciones para administrar certificados: funciones que administran [*almacenes de certificados*](../secgloss/c-gly.md)y funciones que funcionan con los certificados, [*listas de revocación de certificados*](../secgloss/c-gly.md) (CRL) y listas de certificados de [*confianza*](../secgloss/c-gly.md) (CTL) dentro de esos almacenes.</span><span class="sxs-lookup"><span data-stu-id="4018e-108">CryptoAPI offers two main categories of functions for managing certificates: functions that manage [*certificate stores*](../secgloss/c-gly.md), and functions that work with the certificates, [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) within those stores.</span></span>

<span data-ttu-id="4018e-109">Las funciones que administran [*almacenes de certificados*](../secgloss/c-gly.md) incluyen funciones para trabajar con [*almacenes*](../secgloss/v-gly.md)lógicos o virtuales, [*almacenes remotos*](../secgloss/r-gly.md), [*almacenes externos*](../secgloss/e-gly.md)y almacenes que se pueden reubicar.</span><span class="sxs-lookup"><span data-stu-id="4018e-109">The functions that manage [*certificate stores*](../secgloss/c-gly.md) include functions for working with logical or [*virtual stores*](../secgloss/v-gly.md), [*remote stores*](../secgloss/r-gly.md), [*external stores*](../secgloss/e-gly.md), and stores that can be relocated.</span></span>

<span data-ttu-id="4018e-110">Los certificados, las [*CRL*](../secgloss/c-gly.md)y las [*CTL*](../secgloss/c-gly.md) se pueden mantener y mantener en [*almacenes de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4018e-110">Certificates, [*CRLs*](../secgloss/c-gly.md), and [*CTLs*](../secgloss/c-gly.md) can be kept and maintained in [*certificate stores*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="4018e-111">Se pueden recuperar de un almacén donde se han guardado para su uso en procesos de autenticación.</span><span class="sxs-lookup"><span data-stu-id="4018e-111">They can be retrieved from a store where they have been persisted for use in authentication processes.</span></span>

<span data-ttu-id="4018e-112">El [*almacén de certificados*](../secgloss/c-gly.md) es fundamental para toda la funcionalidad de certificado.</span><span class="sxs-lookup"><span data-stu-id="4018e-112">The [*certificate store*](../secgloss/c-gly.md) is central to all certificate functionality.</span></span> <span data-ttu-id="4018e-113">Los certificados se administran en el almacén mediante funciones con un prefijo "cert".</span><span class="sxs-lookup"><span data-stu-id="4018e-113">The certificates are managed in the store using functions with a "Cert" prefix.</span></span> <span data-ttu-id="4018e-114">Un almacén de certificados típico es una lista vinculada de [*certificados*](../secgloss/c-gly.md) , tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="4018e-114">A typical certificate store is a linked list of [*certificates*](../secgloss/c-gly.md) as shown in the following illustration.</span></span>

![almacén de certificados](images/certstore1.png)

<span data-ttu-id="4018e-116">En la ilustración anterior se muestra:</span><span class="sxs-lookup"><span data-stu-id="4018e-116">The preceding illustration shows:</span></span>

-   <span data-ttu-id="4018e-117">Cada [*almacén de certificados*](../secgloss/c-gly.md) tiene un puntero al primer bloque de certificado de ese almacén.</span><span class="sxs-lookup"><span data-stu-id="4018e-117">Each [*certificate store*](../secgloss/c-gly.md) has a pointer to the first certificate block in that store.</span></span>
-   <span data-ttu-id="4018e-118">Un bloque de certificados incluye un puntero a los datos de ese certificado y un puntero "siguiente" al siguiente bloque de certificados del almacén.</span><span class="sxs-lookup"><span data-stu-id="4018e-118">A certificate block includes a pointer to that certificate's data and a "next" pointer to the next certificate block in the store.</span></span>
-   <span data-ttu-id="4018e-119">El puntero "siguiente" en el último bloque de certificado se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="4018e-119">The "next" pointer in the last certificate block is set to **NULL**.</span></span>
-   <span data-ttu-id="4018e-120">El bloque de datos de un certificado contiene el contexto de certificado de solo lectura y las propiedades extendidas del certificado.</span><span class="sxs-lookup"><span data-stu-id="4018e-120">The data block of a certificate contains the read-only certificate context and any extended properties of the certificate.</span></span>
-   <span data-ttu-id="4018e-121">El bloque de datos de cada certificado contiene un [*recuento de referencias*](../secgloss/r-gly.md) que realiza un seguimiento del número de punteros al certificado que existe.</span><span class="sxs-lookup"><span data-stu-id="4018e-121">The data block of each certificate contains a [*reference count*](../secgloss/r-gly.md) that keeps track of the number of pointers to the certificate that exist.</span></span>

<span data-ttu-id="4018e-122">Normalmente, los certificados de un [*almacén de certificados*](../secgloss/c-gly.md) se mantienen en algún tipo de almacenamiento permanente, como un archivo de disco o el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="4018e-122">Certificates in a [*certificate store*](../secgloss/c-gly.md) are normally kept in some kind of permanent storage such as a disk file or the system registry.</span></span> <span data-ttu-id="4018e-123">Los almacenes de certificados también se pueden crear y abrir de forma estricta en la memoria.</span><span class="sxs-lookup"><span data-stu-id="4018e-123">Certificate stores can also be created and opened strictly in memory.</span></span> <span data-ttu-id="4018e-124">Un almacén de memoria proporciona un almacenamiento de certificados temporal para trabajar con certificados que no es necesario mantener.</span><span class="sxs-lookup"><span data-stu-id="4018e-124">A memory store provides temporary certificate storage for working with certificates that do not need to be kept.</span></span>

<span data-ttu-id="4018e-125">Las ubicaciones de almacén adicionales permiten mantener y buscar almacenes en varias partes del registro de un equipo local o, con los permisos adecuados establecidos, en el registro de un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="4018e-125">Additional store locations allow stores to be kept and searched in various parts of a local computer's registry or, with proper permissions set, in the registry on a remote computer.</span></span>

<span data-ttu-id="4018e-126">Cada usuario tiene un almacén personal en el que se almacenan los certificados del usuario.</span><span class="sxs-lookup"><span data-stu-id="4018e-126">Each user has a personal My store where that user's certificates are stored.</span></span> <span data-ttu-id="4018e-127">Mi almacén puede estar en cualquiera de las diversas ubicaciones físicas, incluido el registro en un equipo local o remoto, un archivo de disco, una base de datos, un servicio de directorio, una [*tarjeta inteligente*](../secgloss/s-gly.md)u otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="4018e-127">The My store can be at any one of many physical locations, including the registry on a local or remote computer, a disk file, a database, directory service, a [*smart card*](../secgloss/s-gly.md), or another location.</span></span> <span data-ttu-id="4018e-128">Aunque se puede almacenar cualquier certificado en mi almacén, este almacén se debe reservar para los certificados personales de un usuario: los certificados usados para firmar y descifrar los mensajes del usuario.</span><span class="sxs-lookup"><span data-stu-id="4018e-128">While any certificate can be stored in the My store, this store should be reserved for a user's personal certificates: those certificates used for signing and decrypting that user's messages.</span></span>

<span data-ttu-id="4018e-129">El uso de certificados para la autenticación depende de la emisión de certificados por parte de un emisor de certificados de confianza.</span><span class="sxs-lookup"><span data-stu-id="4018e-129">Using certificates for authentication depends on having certificates issued by some trusted certificate issuer.</span></span> <span data-ttu-id="4018e-130">Normalmente, los certificados de los emisores de certificados de confianza se mantienen en el almacén raíz, que actualmente se mantiene en una subclave del registro.</span><span class="sxs-lookup"><span data-stu-id="4018e-130">Certificates for trusted certificate issuers are typically kept in the Root store, which is currently persisted to a registry subkey.</span></span> <span data-ttu-id="4018e-131">En el contexto de CryptoAPI, el almacén raíz está protegido y los cuadros de diálogo de la interfaz de usuario recuerdan al usuario que coloque solo los certificados de confianza en ese almacén.</span><span class="sxs-lookup"><span data-stu-id="4018e-131">In the CryptoAPI context, the Root store is protected, and user interface dialog boxes remind the user to place only trusted certificates into that store.</span></span> <span data-ttu-id="4018e-132">En situaciones de redes empresariales, un administrador del sistema puede insertar (copiar) certificados desde el equipo del controlador de dominio en los almacenes raíz de los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="4018e-132">In enterprise network situations, certificates might be pushed (copied) by a system administrator from the domain controller computer to the Root stores on client computers.</span></span> <span data-ttu-id="4018e-133">Este proceso proporciona a todos los miembros de un dominio con listas de confianza similares.</span><span class="sxs-lookup"><span data-stu-id="4018e-133">This process provides all members of a domain with similar trust lists.</span></span>

<span data-ttu-id="4018e-134">Otros certificados se pueden almacenar en el almacén del sistema de la [*entidad de certificación*](../secgloss/c-gly.md) (CA) o en almacenes creados por el usuario y basados en archivos.</span><span class="sxs-lookup"><span data-stu-id="4018e-134">Other certificates can be stored in the [*certification authority*](../secgloss/c-gly.md) (CA) system store or in user-created, file-based stores.</span></span>

<span data-ttu-id="4018e-135">Para obtener listas de funciones para usar y mantener almacenes de certificados, consulte [funciones del almacén de certificados](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4018e-135">For lists of functions for using and maintaining certificate stores, see [Certificate Store Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="4018e-136">Para obtener un ejemplo en el que se usan algunas de estas funciones, vea [programa C de ejemplo: operaciones del almacén de certificados](example-c-program-certificate-store-operations.md).</span><span class="sxs-lookup"><span data-stu-id="4018e-136">For an example that uses some of these functions, see [Example C Program: Certificate Store Operations](example-c-program-certificate-store-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4018e-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4018e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4018e-138">Administrar un estado del almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="4018e-138">Managing a Certificate Store State</span></span>](managing-a-certificate-store-state.md)
</dt> <dt>

[<span data-ttu-id="4018e-139">Trabajar con certificados en almacenes de certificados</span><span class="sxs-lookup"><span data-stu-id="4018e-139">Working with Certificates in Certificate Stores</span></span>](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[<span data-ttu-id="4018e-140">Vínculos de certificado</span><span class="sxs-lookup"><span data-stu-id="4018e-140">Certificate Links</span></span>](certificate-links.md)
</dt> <dt>

[<span data-ttu-id="4018e-141">Almacenes de colección</span><span class="sxs-lookup"><span data-stu-id="4018e-141">Collection Stores</span></span>](collection-stores.md)
</dt> <dt>

[<span data-ttu-id="4018e-142">Almacenes lógicos y físicos</span><span class="sxs-lookup"><span data-stu-id="4018e-142">Logical and Physical Stores</span></span>](logical-and-physical-stores.md)
</dt> <dt>

[<span data-ttu-id="4018e-143">Ubicaciones del almacén del sistema</span><span class="sxs-lookup"><span data-stu-id="4018e-143">System Store Locations</span></span>](system-store-locations.md)
</dt> <dt>

[<span data-ttu-id="4018e-144">Migración del almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="4018e-144">Certificate Store Migration</span></span>](certificate-store-migration.md)
</dt> </dl>

 

 

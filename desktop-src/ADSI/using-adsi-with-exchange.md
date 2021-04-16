---
title: Usar ADSI con Exchange
description: Para Exchange 2000, la información sobre el uso de ADSI con Exchange se incluye en el SDK de Exchange 2000. Para obtener más información, vea tareas de administración de ADSI.
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- ADSI para Exchange ADSI
- ADSI para Exchange, buzones de correo
- ADSI para Exchange ADSI, buzones de correo, creación
- ADSI para Exchange, buzones de correo, eliminación
- ADSI para Exchange ADSI, buzones de correo, configuración del descriptor de seguridad
- ADSI para Exchange ADSI, buzones de correo, buscar servidor principal para
- ADSI para Exchange ADSI, obtener y modificar mensajes
- ADSI para Exchange ADSI, descriptores de seguridad
- ADSI para Exchange ADSI, descriptores de seguridad, manipular
- ADSI para Exchange ADSI, descriptores de seguridad, configuración
- ADSI para Exchange, contenedor de destinatarios
- ADSI para Exchange ADSI, ver propiedades de objetos de Exchange
- ADSI para Exchange ADSI, contenedor de destinatarios, personalizado
- ADSI para Exchange, Exchange Server
- ADSI para Exchange ADSI, Exchange Server, ver y modificar esquemas
- ADSI para Exchange ADSI, Exchange Server, enumeración de la versión del servidor
- ADSI para Exchange ADSI, Exchange Server, organización y nombre de sitio
- ADSI para Exchange ADSI, Exchange Server, buscar Mailbox Home Server
- ADSI para Exchange, direcciones de correo electrónico y recuperación
- ADSI para Exchange, listas de distribución, creación
- ADSI para Exchange, entradas ocultas o eliminadas
- ADSI para Exchange ADSI, recuperar cambios del servicio de directorio
- ADSI para Exchange ADSI, tamaño del mensaje
- ADSI para Exchange ADSI, solucionar problemas
- ADSI de buzones de correo
- buzones ADSI, crear
- buzones ADSI, eliminar
- buzones ADSI, establecer el descriptor de seguridad en
- buzones ADSI, buscar servidor principal para
- mensajes ADSI, obtener y modificar
- ADSI de Exchange
- Exchange ADSI, buzones de correo
- Exchange ADSI, buzones de correo, creación
- Exchange ADSI, buzones de correo, eliminación
- Exchange ADSI, buzones de correo y configuración del descriptor de seguridad
- Exchange ADSI, buzones de correo, buscar servidor principal para
- Exchange ADSI, obtener y modificar mensajes
- ADSI de Exchange, descriptores de seguridad
- ADSI de Exchange, descriptores de seguridad, manipular
- ADSI de Exchange, descriptores de seguridad, configuración
- Exchange ADSI, contenedor de destinatarios
- ADSI de Exchange, ver propiedades de objetos de Exchange
- Exchange ADSI, contenedor de destinatarios, personalizado
- Exchange ADSI, Exchange Server
- Exchange ADSI, Exchange Server, ver y modificar esquemas
- Exchange ADSI, Exchange Server, enumeración de la versión del servidor
- Exchange ADSI, Exchange Server, organización y nombre de sitio
- Exchange ADSI, Exchange Server, buscar Mailbox Home Server
- Exchange ADSI, direcciones de correo electrónico, recuperar
- ADSI de Exchange, listas de distribución, creación
- Entradas de ADSI de Exchange, ocultas o eliminadas
- Exchange ADSI, recuperar cambios del servicio de directorio
- ADSI de Exchange, tamaño del mensaje
- Exchange ADSI, solucionar problemas
- descriptores de seguridad ADSI, para objetos de Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833d60c284a12e759eb74b22c9aa48abc75da463
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656406"
---
# <a name="using-adsi-with-exchange"></a><span data-ttu-id="20cfc-159">Usar ADSI con Exchange</span><span class="sxs-lookup"><span data-stu-id="20cfc-159">Using ADSI with Exchange</span></span>

<span data-ttu-id="20cfc-160">Para Exchange 2000, la información sobre el uso de ADSI con Exchange se incluye en el SDK de Exchange 2000.</span><span class="sxs-lookup"><span data-stu-id="20cfc-160">For Exchange 2000, information for using ADSI with Exchange is contained in the Exchange 2000 SDK.</span></span> <span data-ttu-id="20cfc-161">Para obtener más información, vea [tareas de administración de ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="20cfc-161">For more information, see [Management Tasks for ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span></span>

<span data-ttu-id="20cfc-162">En esta sección se pueden encontrar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="20cfc-162">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="20cfc-163">Creación de una dirección URL de usuario</span><span class="sxs-lookup"><span data-stu-id="20cfc-163">Creating a user URL</span></span>
-   <span data-ttu-id="20cfc-164">Crear rutas de acceso Active Directory</span><span class="sxs-lookup"><span data-stu-id="20cfc-164">Building Active Directory paths</span></span>
-   <span data-ttu-id="20cfc-165">Enumerar servidores Exchange 2000 con ADSI</span><span class="sxs-lookup"><span data-stu-id="20cfc-165">Enumerating Exchange 2000 servers with ADSI</span></span>
-   <span data-ttu-id="20cfc-166">Manipular atributos de extensión con ADSI</span><span class="sxs-lookup"><span data-stu-id="20cfc-166">Manipulating extension attributes with ADSI</span></span>
-   <span data-ttu-id="20cfc-167">Agregar o quitar un objeto de administrador con ADSI</span><span class="sxs-lookup"><span data-stu-id="20cfc-167">Adding/removing a manager object with ADSI</span></span>
-   <span data-ttu-id="20cfc-168">Enumerar propiedades de objetos de Exchange con ADSI/ADO</span><span class="sxs-lookup"><span data-stu-id="20cfc-168">Enumerating Exchange object properties with ADSI/ADO</span></span>
-   <span data-ttu-id="20cfc-169">Recuperar un nombre distintivo de Exchange heredado con ADSI</span><span class="sxs-lookup"><span data-stu-id="20cfc-169">Retrieving a legacy Exchange distinguished name with ADSI</span></span>
-   <span data-ttu-id="20cfc-170">Buscar el nombre de la organización de Exchange mediante ADSI</span><span class="sxs-lookup"><span data-stu-id="20cfc-170">Finding the Exchange organization name using ADSI</span></span>
-   <span data-ttu-id="20cfc-171">Búsqueda de listas de direcciones de Exchange con ADSI</span><span class="sxs-lookup"><span data-stu-id="20cfc-171">Finding Exchange address lists with ADSI</span></span>
-   <span data-ttu-id="20cfc-172">Crear una lista de distribución mediante CDOEXM y ADSI</span><span class="sxs-lookup"><span data-stu-id="20cfc-172">Creating a distribution list using CDOEXM and ADSI</span></span>
-   <span data-ttu-id="20cfc-173">Configuración de la restricción de mensajes en un servidor virtual SMTP mediante ADSI</span><span class="sxs-lookup"><span data-stu-id="20cfc-173">Setting message restriction on an SMTP virtual server using ADSI</span></span>

<span data-ttu-id="20cfc-174">En el caso de Exchange 5,5, la referencia ADSI y el uso de la información se pueden encontrar en la guía de [intercambio de ADSI](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) .</span><span class="sxs-lookup"><span data-stu-id="20cfc-174">For Exchange 5.5, the ADSI reference and using information can be found in the [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) guide.</span></span>

<span data-ttu-id="20cfc-175">En esta sección se pueden encontrar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="20cfc-175">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="20cfc-176">Ver y modificar el esquema de Exchange Server</span><span class="sxs-lookup"><span data-stu-id="20cfc-176">Viewing and modifying the Exchange Server Schema</span></span>
-   <span data-ttu-id="20cfc-177">Visualización de las propiedades sin procesar de un objeto de Exchange</span><span class="sxs-lookup"><span data-stu-id="20cfc-177">Viewing the raw properties of an Exchange object</span></span>
-   <span data-ttu-id="20cfc-178">Creación de un buzón de Exchange</span><span class="sxs-lookup"><span data-stu-id="20cfc-178">Creating an Exchange mailbox</span></span>
-   <span data-ttu-id="20cfc-179">Configuración del descriptor de seguridad en un buzón de Exchange</span><span class="sxs-lookup"><span data-stu-id="20cfc-179">Setting the security descriptor on an Exchange mailbox</span></span>
-   <span data-ttu-id="20cfc-180">Manipular los descriptores de seguridad y los SID</span><span class="sxs-lookup"><span data-stu-id="20cfc-180">Manipulating security descriptors and SIDs</span></span>
-   <span data-ttu-id="20cfc-181">Eliminar un objeto de buzón</span><span class="sxs-lookup"><span data-stu-id="20cfc-181">Deleting a mailbox object</span></span>
-   <span data-ttu-id="20cfc-182">Creación de un destinatario personalizado</span><span class="sxs-lookup"><span data-stu-id="20cfc-182">Creating a custom recipient</span></span>
-   <span data-ttu-id="20cfc-183">Creación de un contenedor de destinatarios</span><span class="sxs-lookup"><span data-stu-id="20cfc-183">Creating a recipients container</span></span>
-   <span data-ttu-id="20cfc-184">Obtener el nombre de la organización y del sitio desde un servidor</span><span class="sxs-lookup"><span data-stu-id="20cfc-184">Getting the organization and site name from a server</span></span>
-   <span data-ttu-id="20cfc-185">Mostrar la versión de Exchange Server de todos los servidores de la organización</span><span class="sxs-lookup"><span data-stu-id="20cfc-185">Listing the Exchange server version of all the servers in the organization</span></span>
-   <span data-ttu-id="20cfc-186">Búsqueda del servidor principal de un buzón</span><span class="sxs-lookup"><span data-stu-id="20cfc-186">Finding the home server of a mailbox</span></span>
-   <span data-ttu-id="20cfc-187">Recuperación de direcciones de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="20cfc-187">Retrieving email addresses</span></span>
-   <span data-ttu-id="20cfc-188">Obtener acceso a entradas ocultas o eliminadas</span><span class="sxs-lookup"><span data-stu-id="20cfc-188">Accessing hidden or deleted entries</span></span>
-   <span data-ttu-id="20cfc-189">Recuperando los cambios realizados en el servicio de directorio</span><span class="sxs-lookup"><span data-stu-id="20cfc-189">Retrieving changes made to the directory service</span></span>
-   <span data-ttu-id="20cfc-190">Crear una lista de distribución a partir de los resultados de una consulta</span><span class="sxs-lookup"><span data-stu-id="20cfc-190">Creating a distribution list from the results of a query</span></span>
-   <span data-ttu-id="20cfc-191">Obtener o modificar el tamaño del mensaje</span><span class="sxs-lookup"><span data-stu-id="20cfc-191">Getting or modifying message size</span></span>
-   <span data-ttu-id="20cfc-192">Uso de códigos de error LDAP para solucionar problemas</span><span class="sxs-lookup"><span data-stu-id="20cfc-192">Using LDAP error codes to troubleshoot problems</span></span>

 

 
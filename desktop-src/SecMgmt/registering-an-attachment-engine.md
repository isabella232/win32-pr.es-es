---
description: Antes de que el motor de configuración de seguridad pueda llamar a su motor de datos adjuntos para procesar tareas específicas del servicio, debe instalar el motor de datos adjuntos y registrarlo en el motor de configuración de seguridad.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Registrar un motor de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686677"
---
# <a name="registering-an-attachment-engine"></a><span data-ttu-id="99f93-103">Registrar un motor de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="99f93-103">Registering an Attachment Engine</span></span>

<span data-ttu-id="99f93-104">Antes de que el motor de configuración de seguridad pueda llamar a su motor de datos adjuntos para procesar tareas específicas del servicio, debe instalar el motor de datos adjuntos y registrarlo en el motor de configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="99f93-104">Before the Security Configuration Engine can call your attachment engine to process service-specific tasks, you must install your attachment engine and register it with the Security Configuration Engine.</span></span>

<span data-ttu-id="99f93-105">**Para instalar y registrar la DLL del motor de datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="99f93-105">**To install and register the attachment engine DLL**</span></span>

1.  <span data-ttu-id="99f93-106">Copie el archivo DLL del motor de datos adjuntos en un directorio del sistema.</span><span class="sxs-lookup"><span data-stu-id="99f93-106">Copy the attachment engine DLL to a directory on the system.</span></span> <span data-ttu-id="99f93-107">El directorio preferido es% WINDIR% \\ secedit \\ Attachments.</span><span class="sxs-lookup"><span data-stu-id="99f93-107">The preferred directory is %windir%\\secedit\\attachments.</span></span> <span data-ttu-id="99f93-108">Si este directorio no existe, debe crearlo.</span><span class="sxs-lookup"><span data-stu-id="99f93-108">If this directory does not exist, you should create it.</span></span>
2.  <span data-ttu-id="99f93-109">Cree una clave del registro en el siguiente nodo.</span><span class="sxs-lookup"><span data-stu-id="99f93-109">Create a registry key under the following node.</span></span> <span data-ttu-id="99f93-110">El *nombre del servicio* es el nombre registrado para los datos adjuntos y debe ser el mismo nombre de servicio usado en el administrador de control de servicios, un módulo que administra la detención e inicio de los servicios.</span><span class="sxs-lookup"><span data-stu-id="99f93-110">The *service name* is the registered name for the attachment, and must be the same service name used in the Service Control Manager, a module which manages the stopping and starting of services.</span></span> <span data-ttu-id="99f93-111">El nombre también debe ser único, por lo que no entra en conflicto con los nombres de otros datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="99f93-111">The name must also be unique so it does not conflict with the names of other attachments.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  <span data-ttu-id="99f93-112">Cree el siguiente valor de cadena en la nueva clave del registro.</span><span class="sxs-lookup"><span data-stu-id="99f93-112">Create the following string value in the new registry key.</span></span> <span data-ttu-id="99f93-113">*ruta del motor de datos adjuntos* es la ruta de acceso completa al módulo del motor de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="99f93-113">*attachment engine path* is the full path to the attachment engine module.</span></span><dl> <dd><span data-ttu-id="99f93-114">**ServiceAttachmentPath**  =  *ruta del motor de datos adjuntos*</span><span class="sxs-lookup"><span data-stu-id="99f93-114">**ServiceAttachmentPath** = *attachment engine path*</span></span><dl> <dt>

<span data-ttu-id="99f93-115">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="99f93-115">Data type</span></span>
</dt> <dd><span data-ttu-id="99f93-116">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="99f93-116">REG_SZ</span></span></dd> </dl> </dd> </dl>

 

 




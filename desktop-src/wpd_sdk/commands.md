---
description: Comandos
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Comandos (API de WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275348"
---
# <a name="commands-wpd-api"></a><span data-ttu-id="42afd-103">Comandos (API de WPD)</span><span class="sxs-lookup"><span data-stu-id="42afd-103">Commands (WPD API)</span></span>

<span data-ttu-id="42afd-104">La aplicación cliente y el controlador se comunican mediante los comandos que se envían desde el cliente (a través de la API de dispositivos portátiles de Windows) al controlador (a través del marco de User-Mode driver).</span><span class="sxs-lookup"><span data-stu-id="42afd-104">The client application and the driver communicate by means of commands that are sent from the client (via the Windows Portable Device API) to the driver (via the User-Mode Driver Framework).</span></span> <span data-ttu-id="42afd-105">Un comando puede o no incluir un parámetro y puede devolver o no un resultado.</span><span class="sxs-lookup"><span data-stu-id="42afd-105">A command may or may not include a parameter, and may or may not return a result.</span></span> <span data-ttu-id="42afd-106">Un cliente puede enviar un comando explícitamente, llamando al método [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) o al método **IPortableDeviceService: SendCommand** , o implícitamente, mediante una llamada a cualquiera de los métodos de las interfaces de cliente.</span><span class="sxs-lookup"><span data-stu-id="42afd-106">A client can send a command explicitly, by calling either the [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) method or the **IPortableDeviceService:SendCommand** method, or implicitly, by calling any of the methods of the client interfaces.</span></span> <span data-ttu-id="42afd-107">Algunos comandos solo se pueden enviar explícitamente; Estos se indican en la documentación del comando.</span><span class="sxs-lookup"><span data-stu-id="42afd-107">A few commands can only be sent explicitly; these are noted in the command's documentation.</span></span> <span data-ttu-id="42afd-108">Las páginas de referencia de comandos describen el propósito de un comando, así como los parámetros que espera recibir y los parámetros que se espera que devuelva.</span><span class="sxs-lookup"><span data-stu-id="42afd-108">The command reference pages describe the purpose of a command, as well as what parameters it expects to receive, and what parameters it is expected to return.</span></span>

<span data-ttu-id="42afd-109">Un comando se identifica mediante una estructura **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="42afd-109">A command is identified by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="42afd-110">Se compone de dos partes: una parte GUID (el miembro *fmtid* ) y una parte DWORD (el miembro *PID* ).</span><span class="sxs-lookup"><span data-stu-id="42afd-110">This is made up of two parts: a GUID part (the *fmtid* member) and a DWORD part (the *pid* member).</span></span> <span data-ttu-id="42afd-111">La parte del GUID se usa para indicar la categoría a la que pertenece el comando (los comandos relacionados pertenecen a la misma categoría y, por tanto, tendrán el mismo *fmtid*).</span><span class="sxs-lookup"><span data-stu-id="42afd-111">The GUID part is used to indicate the category the command belongs to (related commands belong to the same category, and therefore will have the same *fmtid*).</span></span> <span data-ttu-id="42afd-112">La parte DWORD indica el identificador del comando y se usa para distinguir los comandos individuales dentro de una categoría de comandos (los valores de *PID* para los comandos de la misma categoría serán diferentes).</span><span class="sxs-lookup"><span data-stu-id="42afd-112">The DWORD part indicates the command ID, and is used to distinguish the individual commands within a command category (the *pid* values for commands in the same category will be different).</span></span>

<span data-ttu-id="42afd-113">En la tabla siguiente se enumeran las categorías de comandos que define Windows portable Devices.</span><span class="sxs-lookup"><span data-stu-id="42afd-113">The following table lists the categories of commands that Windows Portable Devices defines.</span></span> <span data-ttu-id="42afd-114">Los fabricantes de dispositivos pueden definir sus propios comandos mediante la creación de sus propios identificadores de comando y categorías de comandos.</span><span class="sxs-lookup"><span data-stu-id="42afd-114">Device manufacturers can define their own commands by creating their own command categories and command IDs.</span></span> <span data-ttu-id="42afd-115">Sin embargo, un fabricante no debe agregar comandos a las categorías que se enumeran a continuación, ya que están reservadas por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="42afd-115">However, a manufacturer should not add commands to the categories listed below, since these are reserved by Microsoft.</span></span>

<span data-ttu-id="42afd-116">**Categorías de comandos**</span><span class="sxs-lookup"><span data-stu-id="42afd-116">**Command Categories**</span></span>



| <span data-ttu-id="42afd-117">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="42afd-117">Command category</span></span>                         | <span data-ttu-id="42afd-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="42afd-118">Description</span></span>                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42afd-119">**\_categoría \_ común de WPD**</span><span class="sxs-lookup"><span data-stu-id="42afd-119">**WPD\_CATEGORY\_COMMON**</span></span>                | <span data-ttu-id="42afd-120">Comandos comunes a todos los objetos y dispositivos.</span><span class="sxs-lookup"><span data-stu-id="42afd-120">Commands that are common to all objects and devices.</span></span>                                                                                    |
| <span data-ttu-id="42afd-121">**\_categorías de \_ dispositivos de categoría de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="42afd-121">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>         | <span data-ttu-id="42afd-122">Comandos que se usan para recuperar información opcional del dispositivo que se puede usar para mejorar la experiencia del usuario final.</span><span class="sxs-lookup"><span data-stu-id="42afd-122">Commands that are used to retrieve optional device information that can be used to improve end-user experience.</span></span>                         |
| <span data-ttu-id="42afd-123">**\_SMS categoría de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="42afd-123">**WPD\_CATEGORY\_SMS**</span></span>                   | <span data-ttu-id="42afd-124">Comandos que se usan para dispositivos que admiten la funcionalidad de servicio de mensajes cortos (SMS), que normalmente se expone en teléfonos móviles.</span><span class="sxs-lookup"><span data-stu-id="42afd-124">Commands that are used for devices that support short message service (SMS) functionality, which is typically exposed on mobile phones.</span></span> |
| <span data-ttu-id="42afd-125">**\_captura de \_ \_ imagen \_ de la categoría de WPD**</span><span class="sxs-lookup"><span data-stu-id="42afd-125">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span> | <span data-ttu-id="42afd-126">Comandos que se usan para los dispositivos que admiten la captura de imágenes.</span><span class="sxs-lookup"><span data-stu-id="42afd-126">Commands that are used for devices that support still image capture.</span></span>                                                                    |
| <span data-ttu-id="42afd-127">**\_almacenamiento de categorías de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="42afd-127">**WPD\_CATEGORY\_STORAGE**</span></span>               | <span data-ttu-id="42afd-128">Comandos que se usan para los objetos funcionales de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="42afd-128">Commands that are used for storage functional objects.</span></span>                                                                                  |



 

<span data-ttu-id="42afd-129">Los comandos específicos definidos para cada uno de estos tipos se proporcionan en las tablas siguientes, organizadas por tipo de comando.</span><span class="sxs-lookup"><span data-stu-id="42afd-129">The specific commands that are defined for each of these types are given in the following tables, organized by command type.</span></span>

<span data-ttu-id="42afd-130">**\_Categoría común de categoría de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="42afd-130">**WPD\_CATEGORY\_COMMON Category**</span></span>



| <span data-ttu-id="42afd-131">Get-Help</span><span class="sxs-lookup"><span data-stu-id="42afd-131">Command</span></span>                                                                                | <span data-ttu-id="42afd-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="42afd-132">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="42afd-133">**\_dispositivo de \_ \_ restablecimiento común de comandos \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="42afd-133">**WPD\_COMMAND\_COMMON\_RESET\_DEVICE**</span></span>](wpd-command-common-reset-device-command.md) | <span data-ttu-id="42afd-134">Restablece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42afd-134">Resets the device.</span></span> |



 

<span data-ttu-id="42afd-135">**Categoría \_ de \_ sugerencias de dispositivo de categoría de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="42afd-135">**WPD\_CATEGORY\_DEVICE\_HINTS Category**</span></span>



| <span data-ttu-id="42afd-136">Get-Help</span><span class="sxs-lookup"><span data-stu-id="42afd-136">Command</span></span>                                                                                                              | <span data-ttu-id="42afd-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="42afd-137">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="42afd-138">**las \_ sugerencias de dispositivo de comandos WPD \_ obtienen la \_ \_ \_ Ubicación del contenido \_**</span><span class="sxs-lookup"><span data-stu-id="42afd-138">**WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION**</span></span>](wpd-command-device-hints-get-content-location-command.md) | <span data-ttu-id="42afd-139">Recupera los identificadores de objeto de carpetas que pueden contener un objeto de un tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="42afd-139">Retrieves the object IDs of folders that can hold an object of a specified type.</span></span> |



 

<span data-ttu-id="42afd-140">**Categoría de almacenamiento de \_ categoría de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="42afd-140">**WPD\_CATEGORY\_STORAGE Category**</span></span>



| <span data-ttu-id="42afd-141">Get-Help</span><span class="sxs-lookup"><span data-stu-id="42afd-141">Command</span></span>                                                                     | <span data-ttu-id="42afd-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="42afd-142">Description</span></span>                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="42afd-143">**expulsión del almacenamiento de comandos de WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42afd-143">**WPD\_COMMAND\_STORAGE\_EJECT**</span></span>](wpd-command-storage-eject-command.md)   | <span data-ttu-id="42afd-144">Expulsa un medio de almacenamiento que el controlador puede expulsar de forma remota.</span><span class="sxs-lookup"><span data-stu-id="42afd-144">Ejects a storage medium that can be ejected remotely by the driver.</span></span> |
| [<span data-ttu-id="42afd-145">**\_formato de \_ almacenamiento de comandos de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="42afd-145">**WPD\_COMMAND\_STORAGE\_FORMAT**</span></span>](wpd-command-storage-format-command.md) | <span data-ttu-id="42afd-146">Da formato a un objeto funcional de almacenamiento en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42afd-146">Formats a storage functional object on the device.</span></span>                  |



 

<span data-ttu-id="42afd-147">**\_Categoría de SMS categoría de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="42afd-147">**WPD\_CATEGORY\_SMS Category**</span></span>



| <span data-ttu-id="42afd-148">Get-Help</span><span class="sxs-lookup"><span data-stu-id="42afd-148">Command</span></span>                                                         | <span data-ttu-id="42afd-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="42afd-149">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="42afd-150">**comando de WPD \_ \_ SMS \_ send**</span><span class="sxs-lookup"><span data-stu-id="42afd-150">**WPD\_COMMAND\_SMS\_SEND**</span></span>](wpd-command-sms-send-command.md) | <span data-ttu-id="42afd-151">Inicia el envío de un mensaje SMS mediante un objeto funcional de SMS.</span><span class="sxs-lookup"><span data-stu-id="42afd-151">Initiates the sending of an SMS message by an SMS functional object.</span></span> |



 

<span data-ttu-id="42afd-152">**Categoría \_ de \_ \_ captura de imagen \_ de la categoría de WPD**</span><span class="sxs-lookup"><span data-stu-id="42afd-152">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE Category**</span></span>



| <span data-ttu-id="42afd-153">Get-Help</span><span class="sxs-lookup"><span data-stu-id="42afd-153">Command</span></span>                                                                                                   | <span data-ttu-id="42afd-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="42afd-154">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="42afd-155">**\_Inicio de \_ \_ captura de \_ imagen \_ de comando de WPD**</span><span class="sxs-lookup"><span data-stu-id="42afd-155">**WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE**</span></span>](wpd-command-still-image-capture-initiate-command.md) | <span data-ttu-id="42afd-156">Inicia una captura de imagen continua mediante un objeto funcional de imagen fija.</span><span class="sxs-lookup"><span data-stu-id="42afd-156">Initiates a still image capture by a still image functional object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="42afd-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42afd-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42afd-158">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="42afd-158">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




---
description: Este tema contiene información acerca de las API de bajo nivel utilizadas por la infraestructura de cliente de Windows.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Compatibilidad con clientes Low-Level varios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906916"
---
# <a name="miscellaneous-low-level-client-support"></a><span data-ttu-id="3a155-103">Compatibilidad con clientes Low-Level varios</span><span class="sxs-lookup"><span data-stu-id="3a155-103">Miscellaneous Low-Level Client Support</span></span>

<span data-ttu-id="3a155-104">Este tema contiene información acerca de las API de bajo nivel utilizadas por la infraestructura de cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="3a155-104">This topic contains information about low-level APIs that are used by the Windows client infrastructure.</span></span>

### <a name="functions"></a><span data-ttu-id="3a155-105">Functions</span><span class="sxs-lookup"><span data-stu-id="3a155-105">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3a155-106">Tema</span><span class="sxs-lookup"><span data-stu-id="3a155-106">Topic</span></span></th>
<th><span data-ttu-id="3a155-107">Contenido</span><span class="sxs-lookup"><span data-stu-id="3a155-107">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a155-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span></span></td>
<td><span data-ttu-id="3a155-109">La función _lclose cierra el archivo especificado para que ya no esté disponible para lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="3a155-109">The _lclose function closes the specified file so that it is no longer available for reading or writing.</span></span> <span data-ttu-id="3a155-110">Esta función se proporciona por compatibilidad con las versiones de 16 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="3a155-110">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="3a155-111">Las aplicaciones basadas en Win32 deben usar la función CloseHandle.</span><span class="sxs-lookup"><span data-stu-id="3a155-111">Win32-based applications should use the CloseHandle function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span></span></td>
<td><span data-ttu-id="3a155-113">La función _lopen abre un archivo existente y establece el puntero de archivo al principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="3a155-113">The _lopen function opens an existing file and sets the file pointer to the beginning of the file.</span></span> <span data-ttu-id="3a155-114">Esta función se proporciona por compatibilidad con las versiones de 16 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="3a155-114">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="3a155-115">Las aplicaciones basadas en Win32 deben utilizar la función CreateFile.</span><span class="sxs-lookup"><span data-stu-id="3a155-115">Win32-based applications should use the CreateFile function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span></span></td>
<td><span data-ttu-id="3a155-117">La función _lread lee datos del archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="3a155-117">The _lread function reads data from the specified file.</span></span> <span data-ttu-id="3a155-118">Esta función se proporciona por compatibilidad con las versiones de 16 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="3a155-118">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="3a155-119">Las aplicaciones basadas en Win32 deben utilizar la función ReadFile.</span><span class="sxs-lookup"><span data-stu-id="3a155-119">Win32-based applications should use the ReadFile function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span></span></td>
<td><span data-ttu-id="3a155-121">Devuelve un valor que indica si se habilitan los códecs de DVD en el dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="3a155-121">Returns a value indicating whether DVD codecs are enabled on the current device.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span></span></td>
<td><span data-ttu-id="3a155-123">Deshabilita la característica de fantasma de la ventana para el proceso de llamada a la GUI.</span><span class="sxs-lookup"><span data-stu-id="3a155-123">Disables the window ghosting feature for the calling GUI process.</span></span> <span data-ttu-id="3a155-124">El fantasma de las ventanas es una característica del administrador de Windows que permite al usuario minimizar, trasladar o cerrar la ventana principal de una aplicación que no responde.</span><span class="sxs-lookup"><span data-stu-id="3a155-124">Window ghosting is a Windows Manager feature that lets the user minimize, move, or close the main window of an application that is not responding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span></span></td>
<td><span data-ttu-id="3a155-126">Devuelve una lista de propiedades para todos los códecs multimedia instalados en el sistema que cumplan los requisitos especificados.</span><span class="sxs-lookup"><span data-stu-id="3a155-126">Returns a list of properties for all media codecs installed on the system that meet the specified requirements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span></span></td>
<td><span data-ttu-id="3a155-128">Crea una factoría de comunicaciones para registrar una extensión de medios.</span><span class="sxs-lookup"><span data-stu-id="3a155-128">Creates a communication factory for registering a media extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span></span></td>
<td><span data-ttu-id="3a155-130">Crea una instancia de una clase en un paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="3a155-130">Creates an instance of a class in an application package.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span></span></td>
<td><span data-ttu-id="3a155-132">Obtiene un valor que indica si está habilitado el comportamiento multimedia asociado con el GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="3a155-132">Gets a value indicating whether the media behavior associated with the specified GUID is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span></span></td>
<td><span data-ttu-id="3a155-134">En desuso.</span><span class="sxs-lookup"><span data-stu-id="3a155-134">Deprecated.</span></span> <span data-ttu-id="3a155-135">Esta función se utiliza para cerrar el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="3a155-135">This function is used to close the specified handle.</span></span> <span data-ttu-id="3a155-136">El <a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> se sustituye por <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="3a155-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> is superseded by <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span></span></td>
<td><span data-ttu-id="3a155-138">En desuso.</span><span class="sxs-lookup"><span data-stu-id="3a155-138">Deprecated.</span></span> <span data-ttu-id="3a155-139">Compila los descriptores de los búferes proporcionados y pasa los datos sin tipo al controlador de dispositivo asociado al identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="3a155-139">Builds descriptors for the supplied buffer(s) and passes the untyped data to the device driver associated with the file handle.</span></span> <span data-ttu-id="3a155-140"><a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>sustituye a <a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a155-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> is superseded by <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span></span></td>
<td><span data-ttu-id="3a155-142">En desuso.</span><span class="sxs-lookup"><span data-stu-id="3a155-142">Deprecated.</span></span> <span data-ttu-id="3a155-143">Espera hasta que el objeto especificado alcanza un estado de <code>signaled</code> .</span><span class="sxs-lookup"><span data-stu-id="3a155-143">Waits until the specified object attains a state of <code>signaled</code>.</span></span> <span data-ttu-id="3a155-144"><a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>sustituye a <a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a155-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> is superseded by <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="3a155-146">Convierte la cadena de origen ANSI especificada en una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="3a155-146">Converts the specified ANSI source string into a Unicode string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span></span></td>
<td><span data-ttu-id="3a155-148">Convierte una cadena de caracteres en un entero.</span><span class="sxs-lookup"><span data-stu-id="3a155-148">Converts a character string to an integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span></span></td>
<td><span data-ttu-id="3a155-150">Inicializa el búfer proporcionado con una representación de cadena del SID del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="3a155-150">Initializes the supplied buffer with a string representation of the SID for the current user.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="3a155-152">Libera el búfer de cadena asignado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3a155-152">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span></span></td>
<td><span data-ttu-id="3a155-154">Libera el búfer de cadena asignado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3a155-154">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="3a155-156">Libera el búfer de cadena asignado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> o <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.</span><span class="sxs-lookup"><span data-stu-id="3a155-156">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> or by <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span></span></td>
<td><span data-ttu-id="3a155-158">Inicializa una cadena contada.</span><span class="sxs-lookup"><span data-stu-id="3a155-158">Initializes a counted string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="3a155-160">Inicializa una cadena Unicode contada.</span><span class="sxs-lookup"><span data-stu-id="3a155-160">Initializes a counted Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="3a155-162">Convierte la cadena de origen Unicode especificada en una cadena ANSI.</span><span class="sxs-lookup"><span data-stu-id="3a155-162">Converts the specified Unicode source string into an ANSI string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span></span></td>
<td><span data-ttu-id="3a155-164">Esta función convierte la cadena de origen Unicode especificada en una cadena OEM.</span><span class="sxs-lookup"><span data-stu-id="3a155-164">This functions converts the specified Unicode source string into an OEM string.</span></span> <span data-ttu-id="3a155-165">La traducción se realiza con respecto a la página de códigos OEM (OCP).</span><span class="sxs-lookup"><span data-stu-id="3a155-165">The translation is done with respect to the OEM code page (OCP).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span></span></td>
<td><span data-ttu-id="3a155-167">Determina el número de bytes necesarios para representar una cadena Unicode como una cadena ANSI.</span><span class="sxs-lookup"><span data-stu-id="3a155-167">Determines how many bytes are needed to represent a Unicode string as an ANSI string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span></span></td>
<td><span data-ttu-id="3a155-169">La función <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> traduce la cadena Unicode especificada en una nueva cadena de caracteres, usando la página de códigos del formato de transformación Unicode de 8 bits (UTF-8).</span><span class="sxs-lookup"><span data-stu-id="3a155-169">The <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> function translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span></span></td>
<td><span data-ttu-id="3a155-171">La función <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> traduce la cadena de origen especificada en una cadena Unicode, mediante la página de códigos UTF-8.</span><span class="sxs-lookup"><span data-stu-id="3a155-171">The <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> function translates the specified source string into a Unicode string, using the UTF-8 code page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a155-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span></span></td>
<td><span data-ttu-id="3a155-173">Especifica una acción o procesamiento para el editor de métodos de entrada (IME) a través de una subfunción especificada.</span><span class="sxs-lookup"><span data-stu-id="3a155-173">Specifies an action or processing for the Input Method Editor (IME) through a specified subfunction.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3a155-174">Esta función está obsoleta y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="3a155-174">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a155-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a155-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span></span></td>
<td><span data-ttu-id="3a155-176">Habilita o deshabilita temporalmente un IME y, al mismo tiempo, activa o desactiva la visualización de todas las ventanas propiedad del IME.</span><span class="sxs-lookup"><span data-stu-id="3a155-176">Temporarily enables or disables an IME and, at the same time, turns on or off the display of all windows owned by the IME.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3a155-177">Esta función está obsoleta y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="3a155-177">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a><span data-ttu-id="3a155-178">Estructuras</span><span class="sxs-lookup"><span data-stu-id="3a155-178">Structures</span></span>



| <span data-ttu-id="3a155-179">Tema</span><span class="sxs-lookup"><span data-stu-id="3a155-179">Topic</span></span>                                 | <span data-ttu-id="3a155-180">Contenido</span><span class="sxs-lookup"><span data-stu-id="3a155-180">Contents</span></span>                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a155-181">**IMESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="3a155-181">**IMESTRUCT**</span></span>](/windows/win32/api/ime/ns-ime-imestruct) | <span data-ttu-id="3a155-182">Lo usa [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) para especificar la subfunción que se va a ejecutar en el mensaje IME y sus parámetros.</span><span class="sxs-lookup"><span data-stu-id="3a155-182">Used by [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) to specify the subfunction to be executed in the IME message and its parameters.</span></span> <span data-ttu-id="3a155-183">Esta estructura también se usa para recibir los valores devueltos de esas subfunciones.</span><span class="sxs-lookup"><span data-stu-id="3a155-183">This structure is also used to receive return values from those subfunctions.</span></span><br/> |
| [<span data-ttu-id="3a155-184">**String@**</span><span class="sxs-lookup"><span data-stu-id="3a155-184">**STRING**</span></span>](/windows/desktop/api/Winternl/ns-winternl-string)       | <span data-ttu-id="3a155-185">Esta estructura se usa con la función [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) .</span><span class="sxs-lookup"><span data-stu-id="3a155-185">This structure is used with the [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) function.</span></span> <br/>                                                                                                              |



 

### <a name="compiler-routines"></a><span data-ttu-id="3a155-186">Rutinas del compilador</span><span class="sxs-lookup"><span data-stu-id="3a155-186">Compiler Routines</span></span>



| <span data-ttu-id="3a155-187">Tema</span><span class="sxs-lookup"><span data-stu-id="3a155-187">Topic</span></span>                                                             | <span data-ttu-id="3a155-188">Contenido</span><span class="sxs-lookup"><span data-stu-id="3a155-188">Contents</span></span>                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a155-189">**\_\_\_Rutina de controlador específica de C \_**</span><span class="sxs-lookup"><span data-stu-id="3a155-189">**\_\_C\_specific\_handler Routine**</span></span>](--c-specific-handler2.md) | <span data-ttu-id="3a155-190">El [**\_ \_ \_ \_ controlador específico de c**](--c-specific-handler2.md) es una rutina auxiliar para el compilador de c.</span><span class="sxs-lookup"><span data-stu-id="3a155-190">[**\_\_C\_specific\_handler**](--c-specific-handler2.md) is a helper routine for the C compiler.</span></span><br/> |
| [<span data-ttu-id="3a155-191">\_Rutina alldiv</span><span class="sxs-lookup"><span data-stu-id="3a155-191">\_alldiv Routine</span></span>](-win32-alldiv.md)                             | <span data-ttu-id="3a155-192">[ \_ alldiv rutina](-win32-alldiv.md) es una rutina auxiliar para el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="3a155-192">[\_alldiv Routine](-win32-alldiv.md) is a helper routine for the C compiler.</span></span><br/>                     |
| [<span data-ttu-id="3a155-193">\_allmul</span><span class="sxs-lookup"><span data-stu-id="3a155-193">\_allmul</span></span>](-win32-allmul.md) | <span data-ttu-id="3a155-194">Multiplica dos **LONGLONG** o **ULONGLONG**.</span><span class="sxs-lookup"><span data-stu-id="3a155-194">Multiplies two **LONGLONG** or **ULONGLONG**.</span></span> |
| [<span data-ttu-id="3a155-195">\_aulldiv</span><span class="sxs-lookup"><span data-stu-id="3a155-195">\_aulldiv</span></span>](-win32-aulldiv.md) | <span data-ttu-id="3a155-196">Divide dos enteros **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="3a155-196">Divides two **ULONGLONG** integers.</span></span> |
| [<span data-ttu-id="3a155-197">\_Rutina chkstk</span><span class="sxs-lookup"><span data-stu-id="3a155-197">\_chkstk Routine</span></span>](-win32-chkstk.md)                             | <span data-ttu-id="3a155-198">[ \_ chkstk rutina](-win32-chkstk.md) es una rutina auxiliar para el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="3a155-198">[\_chkstk Routine](-win32-chkstk.md) is a helper routine for the C compiler.</span></span><br/>                     |

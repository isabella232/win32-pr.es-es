---
title: App packager (MakeAppx.exe) (Empaquetador de aplicaciones [MakeAppx.exe])
description: El Empaquetador de aplicaciones (MakeAppx.exe) crea un paquete de la aplicación a partir de archivos en disco o extrae los archivos de un paquete de la aplicación en el disco.
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41595550f3bee7b1149959886ed649e9212224b2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149187"
---
# <a name="app-packager-makeappxexe"></a><span data-ttu-id="bccca-103">App packager (MakeAppx.exe) (Empaquetador de aplicaciones [MakeAppx.exe])</span><span class="sxs-lookup"><span data-stu-id="bccca-103">App packager (MakeAppx.exe)</span></span>

> [!Note]  
> <span data-ttu-id="bccca-104">Para obtener instrucciones para UWP sobre el uso de esta herramienta, consulte [crear un paquete de la aplicación con la herramienta MakeAppx.exe](/windows/msix/package/create-app-package-with-makeappx-tool).</span><span class="sxs-lookup"><span data-stu-id="bccca-104">For UWP guidance on using this tool, see [Create an app package with the MakeAppx.exe tool](/windows/msix/package/create-app-package-with-makeappx-tool).</span></span>

 

<span data-ttu-id="bccca-105">El Empaquetador de aplicaciones (MakeAppx.exe) crea un paquete de la aplicación a partir de archivos en disco o extrae los archivos de un paquete de la aplicación en el disco.</span><span class="sxs-lookup"><span data-stu-id="bccca-105">App packager (MakeAppx.exe) creates an app package from files on disk or extracts the files from an app package to disk.</span></span> <span data-ttu-id="bccca-106">A partir de Windows 8.1, el Empaquetador de aplicaciones también crea una agrupación de paquetes de aplicaciones a partir de paquetes de aplicaciones en el disco o extrae los paquetes de la aplicación de una agrupación de paquetes de aplicaciones en el disco.</span><span class="sxs-lookup"><span data-stu-id="bccca-106">Starting with Windows 8.1, App packager also creates an app package bundle from app packages on disk or extracts the app packages from an app package bundle to disk.</span></span> <span data-ttu-id="bccca-107">Se incluye en Microsoft Visual Studio y el kit de desarrollo de software (SDK) de Windows para Windows 8 o el kit de desarrollo de software (SDK) de Windows para Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="bccca-107">It is included in Microsoft Visual Studio and the Windows Software Development Kit (SDK) for Windows 8 or Windows Software Development Kit (SDK) for Windows 8.1.</span></span> <span data-ttu-id="bccca-108">Visite [descargas para que los desarrolladores]( https://msdn.microsoft.com/windows/apps/br229516.aspx) las obtengan.</span><span class="sxs-lookup"><span data-stu-id="bccca-108">Visit [Downloads for developers]( https://msdn.microsoft.com/windows/apps/br229516.aspx) to get them.</span></span>

<span data-ttu-id="bccca-109">La herramienta de MakeAppx.exe se encuentra normalmente en estas ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="bccca-109">The MakeAppx.exe tool is typically found at these locations:</span></span>

-   <span data-ttu-id="bccca-110">En x86: C: \\ archivos de programa (x86) \\ kits de Windows \\ 8,0 \\ bin \\ x86 \\makeappx.exe o C: \\ archivos de programa (x86) \\ kits de Windows \\ 8,1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="bccca-110">On x86: C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
-   <span data-ttu-id="bccca-111">En x64 en dos ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="bccca-111">On x64 in two locations:</span></span>
    -   <span data-ttu-id="bccca-112">C: \\ archivos de programa (x86) \\ kits \\ de Windows 8,0 \\ bin \\ x86 \\makeappx.exe o C: \\ archivos de programa (x86) \\ kits de Windows \\ 8,1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="bccca-112">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
    -   <span data-ttu-id="bccca-113">C: \\ archivos de programa (x86) \\ kits \\ de Windows 8,0 \\ bin \\ x64 \\makeappx.exe o C: \\ archivos de programa (x86) \\ kits de Windows \\ 8,1 \\ bin \\ x64 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="bccca-113">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x64\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x64\\makeappx.exe</span></span>

<span data-ttu-id="bccca-114">No hay ninguna versión ARM de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="bccca-114">There is no ARM version of the tool.</span></span>

-   [<span data-ttu-id="bccca-115">Para crear un paquete con una estructura de directorios</span><span class="sxs-lookup"><span data-stu-id="bccca-115">To create a package using a directory structure</span></span>](#to-create-a-package-using-a-directory-structure)
-   [<span data-ttu-id="bccca-116">Para crear un paquete mediante un archivo de asignación</span><span class="sxs-lookup"><span data-stu-id="bccca-116">To create a package using a mapping file</span></span>](#to-create-a-package-using-a-mapping-file)
-   [<span data-ttu-id="bccca-117">Para firmar el paquete con SignTool</span><span class="sxs-lookup"><span data-stu-id="bccca-117">To sign the package using SignTool</span></span>](#to-sign-the-package-using-signtool)
-   [<span data-ttu-id="bccca-118">Para extraer archivos de un paquete</span><span class="sxs-lookup"><span data-stu-id="bccca-118">To extract files from a package</span></span>](#to-extract-files-from-a-package)
-   [<span data-ttu-id="bccca-119">Para crear una agrupación de paquetes mediante una estructura de directorios</span><span class="sxs-lookup"><span data-stu-id="bccca-119">To create a package bundle using a directory structure</span></span>](#to-create-a-package-bundle-using-a-directory-structure)
-   [<span data-ttu-id="bccca-120">Para crear una agrupación de paquetes mediante un archivo de asignación</span><span class="sxs-lookup"><span data-stu-id="bccca-120">To create a package bundle using a mapping file</span></span>](#to-create-a-package-bundle-using-a-mapping-file)
-   [<span data-ttu-id="bccca-121">Para extraer paquetes de un paquete</span><span class="sxs-lookup"><span data-stu-id="bccca-121">To extract packages from a bundle</span></span>](#to-extract-packages-from-a-bundle)
-   [<span data-ttu-id="bccca-122">Para cifrar un paquete con un archivo de clave</span><span class="sxs-lookup"><span data-stu-id="bccca-122">To encrypt a package with a key file</span></span>](#to-encrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="bccca-123">Para cifrar un paquete con una clave de prueba global</span><span class="sxs-lookup"><span data-stu-id="bccca-123">To encrypt a package with a global test key</span></span>](#to-encrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="bccca-124">Para descifrar un paquete con un archivo de claves</span><span class="sxs-lookup"><span data-stu-id="bccca-124">To decrypt a package with a key file</span></span>](#to-decrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="bccca-125">Para descifrar un paquete con una clave de prueba global</span><span class="sxs-lookup"><span data-stu-id="bccca-125">To decrypt a package with a global test key</span></span>](#to-decrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="bccca-126">Uso</span><span class="sxs-lookup"><span data-stu-id="bccca-126">Usage</span></span>](#usage)

## <a name="using-app-packager"></a><span data-ttu-id="bccca-127">Usar el Empaquetador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="bccca-127">Using App packager</span></span>

> [!Note]  
> <span data-ttu-id="bccca-128">Las rutas de acceso relativas se admiten en toda la herramienta.</span><span class="sxs-lookup"><span data-stu-id="bccca-128">Relative paths are supported throughout the tool.</span></span>

 

### <a name="to-create-a-package-using-a-directory-structure"></a><span data-ttu-id="bccca-129">Para crear un paquete con una estructura de directorios</span><span class="sxs-lookup"><span data-stu-id="bccca-129">To create a package using a directory structure</span></span>

<span data-ttu-id="bccca-130">Coloque el AppxManifest.xml en la raíz de un directorio que contenga todos los archivos de carga de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bccca-130">Place the AppxManifest.xml in the root of a directory containing all of the payload files for your app.</span></span> <span data-ttu-id="bccca-131">Se crea una estructura de directorio idéntica para el paquete de la aplicación y estará disponible cuando el paquete se extraiga en el momento de la implementación.</span><span class="sxs-lookup"><span data-stu-id="bccca-131">An identical directory structure is created for the app package, and will be available when the package is extracted at deployment time.</span></span>

1.  <span data-ttu-id="bccca-132">Coloque todos los archivos en una única estructura de directorios y cree subdirectorios según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="bccca-132">Place all files in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="bccca-133">Cree un manifiesto de paquete válido, AppxManifest.xml y colóquelo en el directorio raíz.</span><span class="sxs-lookup"><span data-stu-id="bccca-133">Create a valid package manifest, AppxManifest.xml, and place it in the root directory.</span></span>

3.  <span data-ttu-id="bccca-134">Ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="bccca-134">Run this command:</span></span>

    <span data-ttu-id="bccca-135">**Paquete de MakeAppx/d** *entrada \_ directoryPath* **/p** _filePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="bccca-135">**MakeAppx pack /d** *input\_directorypath* **/p** _filepath_**.appx**</span></span>

### <a name="to-create-a-package-using-a-mapping-file"></a><span data-ttu-id="bccca-136">Para crear un paquete mediante un archivo de asignación</span><span class="sxs-lookup"><span data-stu-id="bccca-136">To create a package using a mapping file</span></span>

1.  <span data-ttu-id="bccca-137">Cree un manifiesto de paquete válido AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="bccca-137">Create a valid package manifest, AppxManifest.xml.</span></span>

2.  <span data-ttu-id="bccca-138">Cree un archivo de asignación.</span><span class="sxs-lookup"><span data-stu-id="bccca-138">Create a mapping file.</span></span> <span data-ttu-id="bccca-139">La primera línea contiene los **\[ archivos \]** de cadena y las líneas siguientes especifican las rutas de acceso de origen (disco) y de destino (paquete) en cadenas entre comillas.</span><span class="sxs-lookup"><span data-stu-id="bccca-139">The first line contains the string **\[Files\]**, and the lines that follow specify the source (disk) and destination (package) paths in quoted strings.</span></span>

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  <span data-ttu-id="bccca-140">Ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="bccca-140">Run this command:</span></span>

    <span data-ttu-id="bccca-141">**Paquete de MakeAppx/f** *asignando \_ filePath* **/p** _filePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="bccca-141">**MakeAppx pack /f** *mapping\_filepath* **/p** _filepath_**.appx**</span></span>

### <a name="to-sign-the-package-using-signtool"></a><span data-ttu-id="bccca-142">Para firmar el paquete con SignTool</span><span class="sxs-lookup"><span data-stu-id="bccca-142">To sign the package using SignTool</span></span>

1.  <span data-ttu-id="bccca-143">Crea el certificado.</span><span class="sxs-lookup"><span data-stu-id="bccca-143">Create the certificate.</span></span> <span data-ttu-id="bccca-144">El publicador que se muestra en el manifiesto debe coincidir con la información de asunto del publicador del certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="bccca-144">The publisher listed in the manifest must match the publisher subject information of the signing certificate.</span></span> <span data-ttu-id="bccca-145">Para obtener más información sobre cómo crear un certificado de firma, consulte [Cómo crear un certificado de firma de paquete de aplicación](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="bccca-145">For more info about creating a signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

2.  <span data-ttu-id="bccca-146">Ejecute SignTool.exe para firmar el paquete:</span><span class="sxs-lookup"><span data-stu-id="bccca-146">Run SignTool.exe to sign the package:</span></span>

    <span data-ttu-id="bccca-147">**SignTool Sign/a/v/FD**   *nombrearchivocertificado* _filePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="bccca-147">**SignTool sign /a /v /fd** *hashAlgorithm* **/f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="bccca-148">El *hashAlgorithm* debe coincidir con el algoritmo hash usado para crear el blockmap cuando la aplicación se ha empaquetado.</span><span class="sxs-lookup"><span data-stu-id="bccca-148">The *hashAlgorithm* must match the hash algorithm used to create the blockmap when the app was packaged.</span></span> <span data-ttu-id="bccca-149">Con la utilidad de empaquetado de MakeAppx, el algoritmo hash blockmap de appx predeterminado es **SHA256**.</span><span class="sxs-lookup"><span data-stu-id="bccca-149">With the MakeAppx packaging utility, the default Appx blockmap hash algorithm is **SHA256**.</span></span> <span data-ttu-id="bccca-150">Ejecute SignTool.exe especificando **SHA256** como el algoritmo de síntesis de archivo (/FD):</span><span class="sxs-lookup"><span data-stu-id="bccca-150">Run SignTool.exe specifying **SHA256** as the file digest (/fd) algorithm:</span></span>

    <span data-ttu-id="bccca-151">**SignTool signo/a/v/FD** *nombrearchivocertificado* _filePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="bccca-151">**SignTool sign /a /v /fd SHA256 /f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="bccca-152">Para obtener más información sobre cómo firmar paquetes, consulte [cómo firmar un paquete de aplicación mediante SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="bccca-152">For more info about how to sign packages, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span>

### <a name="to-extract-files-from-a-package"></a><span data-ttu-id="bccca-153">Para extraer archivos de un paquete</span><span class="sxs-lookup"><span data-stu-id="bccca-153">To extract files from a package</span></span>

1.  <span data-ttu-id="bccca-154">Ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="bccca-154">Run this command:</span></span>

    <span data-ttu-id="bccca-155">**MakeAppx unpack/p** _File_**. appx/d** *\_ Directorio de salida*</span><span class="sxs-lookup"><span data-stu-id="bccca-155">**MakeAppx unpack /p** _file_**.appx /d** *output\_directory*</span></span>

2.  <span data-ttu-id="bccca-156">El paquete desempaquetado tiene la misma estructura que el paquete instalado.</span><span class="sxs-lookup"><span data-stu-id="bccca-156">The unpacked package has the same structure as the installed package.</span></span>

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a><span data-ttu-id="bccca-157">Para crear una agrupación de paquetes mediante una estructura de directorios</span><span class="sxs-lookup"><span data-stu-id="bccca-157">To create a package bundle using a directory structure</span></span>

<span data-ttu-id="bccca-158">Usamos el comando de **agrupación** para crear un lote de aplicaciones en</span><span class="sxs-lookup"><span data-stu-id="bccca-158">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="bccca-159">agregando todos los paquetes de <content directory> (incluidas las subcarpetas).</span><span class="sxs-lookup"><span data-stu-id="bccca-159">by adding all packages from <content directory> (including subfolders).</span></span> <span data-ttu-id="bccca-160">Si <content directory> contiene un manifiesto de agrupación, AppxBundleManifest.xml, se omite.</span><span class="sxs-lookup"><span data-stu-id="bccca-160">If <content directory> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="bccca-161">Coloque todos los paquetes en una única estructura de directorios y cree subdirectorios según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="bccca-161">Place all packages in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="bccca-162">Ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="bccca-162">Run this command:</span></span>

    <span data-ttu-id="bccca-163">**Paquete de MakeAppx/d** *entrada \_ directoryPath* **/p** _filePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="bccca-163">**MakeAppx bundle /d** *input\_directorypath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a><span data-ttu-id="bccca-164">Para crear una agrupación de paquetes mediante un archivo de asignación</span><span class="sxs-lookup"><span data-stu-id="bccca-164">To create a package bundle using a mapping file</span></span>

<span data-ttu-id="bccca-165">Usamos el comando de **agrupación** para crear un lote de aplicaciones en</span><span class="sxs-lookup"><span data-stu-id="bccca-165">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="bccca-166">agregando todos los paquetes de una lista de paquetes dentro de <mapping file> .</span><span class="sxs-lookup"><span data-stu-id="bccca-166">by adding all packages from a list of packages within <mapping file>.</span></span> <span data-ttu-id="bccca-167">Si <mapping file> contiene un manifiesto de agrupación, AppxBundleManifest.xml, se omite.</span><span class="sxs-lookup"><span data-stu-id="bccca-167">If <mapping file> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="bccca-168">Creará un control <mapping file>.</span><span class="sxs-lookup"><span data-stu-id="bccca-168">Create a <mapping file>.</span></span> <span data-ttu-id="bccca-169">La primera línea contiene los **\[ archivos \]** de cadena y las líneas siguientes especifican los paquetes que se van a agregar a la agrupación.</span><span class="sxs-lookup"><span data-stu-id="bccca-169">The first line contains the string **\[Files\]**, and the lines that follow specify the packages to add to the bundle.</span></span> <span data-ttu-id="bccca-170">Cada paquete se describe mediante un par de rutas de acceso entre comillas, separadas por espacios o tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="bccca-170">Each package is described by a pair of paths in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="bccca-171">El par de rutas de acceso representa el origen del paquete (en disco) y el destino (en la agrupación).</span><span class="sxs-lookup"><span data-stu-id="bccca-171">The pair of paths represents the package's source (on disk) and destination (in bundle).</span></span> <span data-ttu-id="bccca-172">Todos los nombres de paquetes de destino deben tener la extensión. appx.</span><span class="sxs-lookup"><span data-stu-id="bccca-172">All destination package names must have the .appx extension.</span></span>

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  <span data-ttu-id="bccca-173">Ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="bccca-173">Run this command:</span></span>

    <span data-ttu-id="bccca-174">**Paquete de MakeAppx** : *asignación de \_ filePath* **/p** _filePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="bccca-174">**MakeAppx bundle /f** *mapping\_filepath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-extract-packages-from-a-bundle"></a><span data-ttu-id="bccca-175">Para extraer paquetes de un paquete</span><span class="sxs-lookup"><span data-stu-id="bccca-175">To extract packages from a bundle</span></span>

1.  <span data-ttu-id="bccca-176">Ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="bccca-176">Run this command:</span></span>

    <span data-ttu-id="bccca-177">**Desagrupación de MakeAppx/p** _\_ nombre de lote_**. appxbundle/d** *\_ Directorio de salida*</span><span class="sxs-lookup"><span data-stu-id="bccca-177">**MakeAppx unbundle /p** _bundle\_name_**.appxbundle /d** *output\_directory*</span></span>

2.  <span data-ttu-id="bccca-178">La agrupación desempaquetada tiene la misma estructura que el paquete de paquetes instalado.</span><span class="sxs-lookup"><span data-stu-id="bccca-178">The unpacked bundle has the same structure as the installed package bundle.</span></span>

### <a name="to-encrypt-a-package-with-a-key-file"></a><span data-ttu-id="bccca-179">Para cifrar un paquete con un archivo de clave</span><span class="sxs-lookup"><span data-stu-id="bccca-179">To encrypt a package with a key file</span></span>

1.  <span data-ttu-id="bccca-180">Cree un archivo de clave.</span><span class="sxs-lookup"><span data-stu-id="bccca-180">Create a key file.</span></span> <span data-ttu-id="bccca-181">Los archivos de clave deben comenzar con una línea que contenga la cadena " \[ Keys \] " seguida de las líneas que describen las claves con las que se va a cifrar el paquete.</span><span class="sxs-lookup"><span data-stu-id="bccca-181">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="bccca-182">Cada clave se describe mediante un par de cadenas entre comillas, separadas por espacios o tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="bccca-182">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="bccca-183">La primera cadena representa el identificador de clave y la segunda cadena representa la clave de cifrado en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="bccca-183">The first string represents the key ID and the second string represents the encryption key in hexadecimal form.</span></span>

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  <span data-ttu-id="bccca-184">Ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="bccca-184">Run this command:</span></span>

    <span data-ttu-id="bccca-185">**MakeAppx.exe cifrar/p** _\_ nombre del paquete_**. appx/EP** _cifrado \_ \_ nombre del paquete_**. eappx/KF** _keyfile \_ nombre_**. txt**</span><span class="sxs-lookup"><span data-stu-id="bccca-185">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="bccca-186">El paquete de entrada se cifrará en el paquete cifrado especificado mediante el archivo de clave proporcionado.</span><span class="sxs-lookup"><span data-stu-id="bccca-186">The input package will be encrypted into the specified encrypted package using the provided key file.</span></span>

### <a name="to-encrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="bccca-187">Para cifrar un paquete con una clave de prueba global</span><span class="sxs-lookup"><span data-stu-id="bccca-187">To encrypt a package with a global test key</span></span>

1.  <span data-ttu-id="bccca-188">Ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="bccca-188">Run this command:</span></span>

    <span data-ttu-id="bccca-189">**MakeAppx.exe cifrar/p** _\_ nombre del paquete_**. appx/EP** _\_ \_ nombre del paquete cifrado_**. eappx/KT**</span><span class="sxs-lookup"><span data-stu-id="bccca-189">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="bccca-190">El paquete de entrada se cifrará en el paquete cifrado especificado mediante la clave de prueba global.</span><span class="sxs-lookup"><span data-stu-id="bccca-190">The input package will be encrypted into the specified encrypted package using the global test key.</span></span>

### <a name="to-decrypt-a-package-with-a-key-file"></a><span data-ttu-id="bccca-191">Para descifrar un paquete con un archivo de claves</span><span class="sxs-lookup"><span data-stu-id="bccca-191">To decrypt a package with a key file</span></span>

1.  <span data-ttu-id="bccca-192">Cree un archivo de clave.</span><span class="sxs-lookup"><span data-stu-id="bccca-192">Create a key file.</span></span> <span data-ttu-id="bccca-193">Los archivos de clave deben comenzar con una línea que contenga la cadena " \[ Keys \] " seguida de las líneas que describen las claves con las que se va a cifrar el paquete.</span><span class="sxs-lookup"><span data-stu-id="bccca-193">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="bccca-194">Cada clave se describe mediante un par de cadenas entre comillas, separadas por espacios o tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="bccca-194">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="bccca-195">La primera cadena representa el identificador de clave de 32 bytes codificado en Base64 y la segunda cadena representa la clave de cifrado de 32 bytes codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="bccca-195">The first string represents the base64 encoded 32-byte key ID and the second string represents the base64 encoded 32-byte encryption key.</span></span>

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  <span data-ttu-id="bccca-196">Ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="bccca-196">Run this command:</span></span>

    <span data-ttu-id="bccca-197">**MakeAppx.exe descifrar/p** _\_ nombre del paquete_**. appx/EP no** _cifrado \_ \_ nombre del paquete_**. eappx/KF** _keyfile \_ nombre_**. txt**</span><span class="sxs-lookup"><span data-stu-id="bccca-197">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="bccca-198">El paquete de entrada se descifrará en el paquete no cifrado especificado mediante el archivo de clave proporcionado.</span><span class="sxs-lookup"><span data-stu-id="bccca-198">The input package will be decrypted into the specified unencrypted package using the provided key file.</span></span>

### <a name="to-decrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="bccca-199">Para descifrar un paquete con una clave de prueba global</span><span class="sxs-lookup"><span data-stu-id="bccca-199">To decrypt a package with a global test key</span></span>

1.  <span data-ttu-id="bccca-200">Ejecute este comando:</span><span class="sxs-lookup"><span data-stu-id="bccca-200">Run this command:</span></span>

    <span data-ttu-id="bccca-201">**MakeAppx.exe descifrar/p** _\_ nombre del paquete_**. appx/EP** _\_ \_ nombre del paquete sin cifrar_**. eappx/KT**</span><span class="sxs-lookup"><span data-stu-id="bccca-201">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="bccca-202">El paquete de entrada se descifrará en el paquete no cifrado especificado con la clave de prueba global.</span><span class="sxs-lookup"><span data-stu-id="bccca-202">The input package will be decrypted into the specified unencrypted package using the global test key.</span></span>

## <a name="usage"></a><span data-ttu-id="bccca-203">Uso</span><span class="sxs-lookup"><span data-stu-id="bccca-203">Usage</span></span>

<span data-ttu-id="bccca-204">El argumento de línea de comandos **/p** siempre es necesario, con **/d**, **/f** o **/EP**.</span><span class="sxs-lookup"><span data-stu-id="bccca-204">The command line argument **/p** is always required, with either **/d**, **/f**, or **/ep**.</span></span> <span data-ttu-id="bccca-205">Tenga en cuenta que **/d**, **/f** y **/EP** son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="bccca-205">Note that **/d**, **/f**, and **/ep** are mutually exclusive.</span></span>

<span data-ttu-id="bccca-206">**\[ Opciones \] del paquete de MakeAppx** **/p** *\<output package name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="bccca-206">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="bccca-207">**\[ Opciones \] del paquete de MakeAppx** **/p** *\<output package name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="bccca-207">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="bccca-208">**\[ Opciones \] de desempaquetado de MakeAppx** **/p** *\<input package name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="bccca-208">**MakeAppx unpack \[options\]** **/p** *\<input package name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="bccca-209">**\[ Opciones \] de agrupación de MakeAppx** **/p** *\<output bundle name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="bccca-209">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="bccca-210">**\[ Opciones \] de agrupación de MakeAppx** **/p** *\<output bundle name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="bccca-210">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="bccca-211">**\[ Opciones \] de desagrupación de MakeAppx** **/p** *\<input bundle name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="bccca-211">**MakeAppx unbundle \[options\]** **/p** *\<input bundle name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="bccca-212">**\[ Opciones \] de cifrado de MakeAppx** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="bccca-212">**MakeAppx encrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

<span data-ttu-id="bccca-213">**\[ Opciones \] de descifrado de MakeAppx** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="bccca-213">**MakeAppx decrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="bccca-214">Sintaxis de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="bccca-214">Command-line Syntax</span></span>

<span data-ttu-id="bccca-215">Esta es la sintaxis de uso común de línea de comandos para MakeAppx.</span><span class="sxs-lookup"><span data-stu-id="bccca-215">Here is the command-line common usage syntax for MakeAppx.</span></span>

<span data-ttu-id="bccca-216">Paquete de MakeAppx desempaquetar agrupación desempaquetar **\[ \| \| \| \| cifrar cifrar el \| descifrado \]** \[ **/h** **/KF** **/KT** **/l** **/o** **/no** **/NV** **/v** **/pfn** **/?**\]</span><span class="sxs-lookup"><span data-stu-id="bccca-216">**MakeAppx \[pack\|unpack\|bundle\|unbundle\|encrypt\|decrypt\]** \[**/h** **/kf** **/kt** **/l** **/o** **/no** **/nv** **/v** **/pfn** **/?**\]</span></span>

<span data-ttu-id="bccca-217">Los paquetes de **MakeAppx** o desempaquetan los archivos de un paquete, empaquetan o desempaquetan los paquetes de una agrupación, o cifran o descifran el paquete o el lote de la aplicación en el directorio de entrada o archivo de asignación especificado.</span><span class="sxs-lookup"><span data-stu-id="bccca-217">**MakeAppx** packs or unpacks the files in a package, bundles or unbundles the packages in a bundle, or encrypts or decrypts the app package or bundle in the specified input directory or mapping file.</span></span> <span data-ttu-id="bccca-218">Esta es la lista de parámetros que se aplican al **paquete de makeappx**, **desempaquetamiento de makeappx**, paquete de **makeappx**, **desagrupación de makeappx**, **cifrado** de makeappx o **descifrado de makeappx**.</span><span class="sxs-lookup"><span data-stu-id="bccca-218">Here is the list of parameters that apply to **MakeAppx pack**, **MakeAppx unpack**, **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, or **MakeAppx decrypt**.</span></span>

<dl> <dt>

<span data-ttu-id="bccca-219"><span id="_l"></span><span id="_L"></span>**l**</span><span class="sxs-lookup"><span data-stu-id="bccca-219"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="bccca-220">Esta opción se usa para los paquetes localizados.</span><span class="sxs-lookup"><span data-stu-id="bccca-220">This option is used for localized packages.</span></span> <span data-ttu-id="bccca-221">La validación predeterminados se desactiva en paquetes localizados.</span><span class="sxs-lookup"><span data-stu-id="bccca-221">The default validation trips on localized packages.</span></span> <span data-ttu-id="bccca-222">Esta opción deshabilita solo esa validación específica, sin requerir que se deshabilite toda la validación.</span><span class="sxs-lookup"><span data-stu-id="bccca-222">This option disables only that specific validation, without requiring that all validation be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="bccca-223"><span id="_o"></span><span id="_O"></span>**/o**</span><span class="sxs-lookup"><span data-stu-id="bccca-223"><span id="_o"></span><span id="_O"></span>**/o**</span></span>
</dt> <dd>

<span data-ttu-id="bccca-224">Sobrescriba el archivo de salida si existe.</span><span class="sxs-lookup"><span data-stu-id="bccca-224">Overwrite the output file if it exists.</span></span> <span data-ttu-id="bccca-225">Si no se especifica esta opción o la opción **/no** , se pregunta al usuario si desea sobrescribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="bccca-225">If you don't specify this option or the **/no** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="bccca-226">No se puede usar esta opción con **/no**.</span><span class="sxs-lookup"><span data-stu-id="bccca-226">You can't use this option with **/no**.</span></span>

</dd> <dt>

<span data-ttu-id="bccca-227"><span id="_no"></span><span id="_NO"></span>**/no**</span><span class="sxs-lookup"><span data-stu-id="bccca-227"><span id="_no"></span><span id="_NO"></span>**/no**</span></span>
</dt> <dd>

<span data-ttu-id="bccca-228">Se impide que se sobrescriba el archivo de salida, si lo hay.</span><span class="sxs-lookup"><span data-stu-id="bccca-228">Prevents an overwrite of the output file if it exists.</span></span> <span data-ttu-id="bccca-229">Si no se especifica esta opción o la opción **/o** , se pregunta al usuario si desea sobrescribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="bccca-229">If you don't specify this option or the **/o** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="bccca-230">No puede usar esta opción con **/o**.</span><span class="sxs-lookup"><span data-stu-id="bccca-230">You can't use this option with **/o**.</span></span>

</dd> <dt>

<span data-ttu-id="bccca-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span><span class="sxs-lookup"><span data-stu-id="bccca-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span></span>
</dt> <dd>

<span data-ttu-id="bccca-232">Omitir la validación semántica.</span><span class="sxs-lookup"><span data-stu-id="bccca-232">Skip semantic validation.</span></span> <span data-ttu-id="bccca-233">Si no se especifica esta opción, la herramienta realiza una validación completa del paquete.</span><span class="sxs-lookup"><span data-stu-id="bccca-233">If you don't specify this option, the tool performs a full validation of the package.</span></span>

</dd> <dt>

<span data-ttu-id="bccca-234"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="bccca-234"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="bccca-235">Habilite la salida del registro detallado en la consola.</span><span class="sxs-lookup"><span data-stu-id="bccca-235">Enable verbose logging output to the console.</span></span>

</dd> <dt>

<span data-ttu-id="bccca-236"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="bccca-236"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="bccca-237">Mostrar texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="bccca-237">Display help text.</span></span>

</dd> </dl>

<span data-ttu-id="bccca-238">**El paquete de makeappx** , el desempaquetado de **makeappx** , el paquete de **makeappx**, el **desempaquetado** de makeappx, el **cifrado de makeappx** y el **descifrado de makeappx** son comandos mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="bccca-238">**MakeAppx pack** , **MakeAppx unpack** , **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, and **MakeAppx decrypt** are mutually exclusive commands.</span></span> <span data-ttu-id="bccca-239">Estos son los parámetros de línea de comandos que se aplican específicamente a cada comando:</span><span class="sxs-lookup"><span data-stu-id="bccca-239">Here are the command-line parameters that apply specifically to each command:</span></span>

<span data-ttu-id="bccca-240">**Paquete** \[ de MakeAppx **h**\]</span><span class="sxs-lookup"><span data-stu-id="bccca-240">**MakeAppx pack** \[**h**\]</span></span>

<span data-ttu-id="bccca-241">Crea un paquete.</span><span class="sxs-lookup"><span data-stu-id="bccca-241">Creates a package.</span></span>

<dl> <dt>

<span data-ttu-id="bccca-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span> *algoritmo* /h</span><span class="sxs-lookup"><span data-stu-id="bccca-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** *algorithm*</span></span>
</dt> <dd>

<span data-ttu-id="bccca-243">Especifica el algoritmo hash que usar al crear la asignación de bloques.</span><span class="sxs-lookup"><span data-stu-id="bccca-243">Specifies the hash algorithm to use when creating the block map.</span></span> <span data-ttu-id="bccca-244">Estos son los valores válidos para el *algoritmo*:</span><span class="sxs-lookup"><span data-stu-id="bccca-244">Here are valid values for *algorithm*:</span></span>

<dl> <dd><span data-ttu-id="bccca-245">SHA256 (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="bccca-245">SHA256 (default)</span></span></dd> <dd><span data-ttu-id="bccca-246">SHA384</span><span class="sxs-lookup"><span data-stu-id="bccca-246">SHA384</span></span></dd> <dd><span data-ttu-id="bccca-247">SHA512</span><span class="sxs-lookup"><span data-stu-id="bccca-247">SHA512</span></span></dd> </dl>

<span data-ttu-id="bccca-248">No puede usar esta opción con el comando **unpack** .</span><span class="sxs-lookup"><span data-stu-id="bccca-248">You can't use this option with the **unpack** command.</span></span>

</dd> </dl>

<span data-ttu-id="bccca-249">**Desempaquetar MakeAppx** \[ **pfn**\]</span><span class="sxs-lookup"><span data-stu-id="bccca-249">**MakeAppx unpack** \[**pfn**\]</span></span>

<span data-ttu-id="bccca-250">Extrae todos los archivos del paquete especificado en el directorio de salida especificado.</span><span class="sxs-lookup"><span data-stu-id="bccca-250">Extracts all files in the specified package to the specified output directory.</span></span> <span data-ttu-id="bccca-251">La salida tiene la misma estructura de directorios que el paquete.</span><span class="sxs-lookup"><span data-stu-id="bccca-251">The output has the same directory structure as the package.</span></span>

<dl> <dt>

<span data-ttu-id="bccca-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="bccca-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="bccca-253">Especifica un directorio denominado con el nombre completo del paquete.</span><span class="sxs-lookup"><span data-stu-id="bccca-253">Specifies a directory named with the package full name.</span></span> <span data-ttu-id="bccca-254">Este directorio se crea en la ubicación de salida proporcionada.</span><span class="sxs-lookup"><span data-stu-id="bccca-254">This directory is created under the provided output location.</span></span> <span data-ttu-id="bccca-255">No puede usar esta opción con el comando **Pack** .</span><span class="sxs-lookup"><span data-stu-id="bccca-255">You can't use this option with the **pack** command.</span></span>

</dd> </dl>

<span data-ttu-id="bccca-256">**Desagrupación** \[ de MakeAppx **pfn**\]</span><span class="sxs-lookup"><span data-stu-id="bccca-256">**MakeAppx unbundle** \[**pfn**\]</span></span>

<span data-ttu-id="bccca-257">Desempaqueta todos los paquetes en un subdirectorio de la ruta de acceso de salida especificada, con el nombre completo del paquete.</span><span class="sxs-lookup"><span data-stu-id="bccca-257">Unpacks all packages to a subdirectory under the specified output path, named after the bundle full name.</span></span> <span data-ttu-id="bccca-258">La salida tiene la misma estructura de directorios que el paquete de paquetes instalado.</span><span class="sxs-lookup"><span data-stu-id="bccca-258">The output has the same directory structure as the installed package bundle.</span></span>

<dl> <dt>

<span data-ttu-id="bccca-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="bccca-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="bccca-260">Especifica un directorio denominado con el nombre completo de la agrupación de paquetes.</span><span class="sxs-lookup"><span data-stu-id="bccca-260">Specifies a directory named with the package bundle full name.</span></span> <span data-ttu-id="bccca-261">Este directorio se crea en la ubicación de salida proporcionada.</span><span class="sxs-lookup"><span data-stu-id="bccca-261">This directory is created under the provided output location.</span></span> <span data-ttu-id="bccca-262">No se puede usar esta opción con el comando **bundle** .</span><span class="sxs-lookup"><span data-stu-id="bccca-262">You can't use this option with the **bundle** command.</span></span>

</dd> </dl>

<span data-ttu-id="bccca-263">**Cifrado** \[ de MakeAppx **KF**, **KT**\]</span><span class="sxs-lookup"><span data-stu-id="bccca-263">**MakeAppx encrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="bccca-264">Crea un paquete de aplicación cifrada a partir del paquete de la aplicación de entrada especificado en el paquete de salida especificado.</span><span class="sxs-lookup"><span data-stu-id="bccca-264">Creates an encrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="bccca-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/KF\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="bccca-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="bccca-266">Cifra el paquete o agrupación utilizando la clave del archivo de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="bccca-266">Encrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="bccca-267">Esta opción no se puede usar con **KT**.</span><span class="sxs-lookup"><span data-stu-id="bccca-267">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="bccca-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="bccca-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="bccca-269">Cifra el paquete o agrupación mediante la clave de prueba global.</span><span class="sxs-lookup"><span data-stu-id="bccca-269">Encrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="bccca-270">Esta opción no se puede usar con **KF**.</span><span class="sxs-lookup"><span data-stu-id="bccca-270">You can't use this option with **kf**.</span></span>

</dd> </dl>

<span data-ttu-id="bccca-271">**Descifrado** \[ de MakeAppx **KF**, **KT**\]</span><span class="sxs-lookup"><span data-stu-id="bccca-271">**MakeAppx decrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="bccca-272">Crea un paquete de aplicación sin cifrar a partir del paquete de la aplicación de entrada especificado en el paquete de salida especificado.</span><span class="sxs-lookup"><span data-stu-id="bccca-272">Creates an unencrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="bccca-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/KF\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="bccca-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="bccca-274">Descifra el paquete o agrupación utilizando la clave del archivo de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="bccca-274">Decrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="bccca-275">Esta opción no se puede usar con **KT**.</span><span class="sxs-lookup"><span data-stu-id="bccca-275">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="bccca-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="bccca-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="bccca-277">Descifra el paquete o agrupación mediante la clave de prueba global.</span><span class="sxs-lookup"><span data-stu-id="bccca-277">Decrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="bccca-278">Esta opción no se puede usar con **KF**.</span><span class="sxs-lookup"><span data-stu-id="bccca-278">You can't use this option with **kf**.</span></span>

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a><span data-ttu-id="bccca-279">Validación semántica realizada por MakeAppx</span><span class="sxs-lookup"><span data-stu-id="bccca-279">Semantic validation performed by MakeAppx</span></span>

<span data-ttu-id="bccca-280">MakeAppx realiza una validación semántica limitada que está diseñada para detectar los errores de implementación más comunes y ayudar a garantizar que el paquete de la aplicación es válido.</span><span class="sxs-lookup"><span data-stu-id="bccca-280">MakeAppx performs limited semantic validation that is designed to catch the most common deployment errors and help ensure that the app package is valid.</span></span>

<span data-ttu-id="bccca-281">Esta validación garantiza que:</span><span class="sxs-lookup"><span data-stu-id="bccca-281">This validation ensures that:</span></span>

-   <span data-ttu-id="bccca-282">Todos los archivos a los que se hace referencia en el manifiesto del paquete se incluyen en el paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bccca-282">All files referenced in the package manifest are included in the app package.</span></span>
-   <span data-ttu-id="bccca-283">Una aplicación no tiene dos claves idénticas.</span><span class="sxs-lookup"><span data-stu-id="bccca-283">An application does not have two identical keys.</span></span>
-   <span data-ttu-id="bccca-284">Una aplicación no se registra para un protocolo prohibido en esta lista: SMB, archivo, MS-WWA-WEB, MS-WWA.</span><span class="sxs-lookup"><span data-stu-id="bccca-284">An application does not register for a forbidden protocol from this list: SMB , FILE, MS-WWA-WEB, MS-WWA.</span></span>

<span data-ttu-id="bccca-285">Esta validación semántica no está completa y no se garantiza que los paquetes compilados por MakeAppx sean instalables.</span><span class="sxs-lookup"><span data-stu-id="bccca-285">This semantic validation is not complete, and packages built by MakeAppx are not guaranteed to be installable.</span></span>

 

 
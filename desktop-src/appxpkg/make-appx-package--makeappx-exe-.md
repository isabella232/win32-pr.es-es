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
# <a name="app-packager-makeappxexe"></a>App packager (MakeAppx.exe) (Empaquetador de aplicaciones [MakeAppx.exe])

> [!Note]  
> Para obtener instrucciones para UWP sobre el uso de esta herramienta, consulte [crear un paquete de la aplicación con la herramienta MakeAppx.exe](/windows/msix/package/create-app-package-with-makeappx-tool).

 

El Empaquetador de aplicaciones (MakeAppx.exe) crea un paquete de la aplicación a partir de archivos en disco o extrae los archivos de un paquete de la aplicación en el disco. A partir de Windows 8.1, el Empaquetador de aplicaciones también crea una agrupación de paquetes de aplicaciones a partir de paquetes de aplicaciones en el disco o extrae los paquetes de la aplicación de una agrupación de paquetes de aplicaciones en el disco. Se incluye en Microsoft Visual Studio y el kit de desarrollo de software (SDK) de Windows para Windows 8 o el kit de desarrollo de software (SDK) de Windows para Windows 8.1. Visite [descargas para que los desarrolladores]( https://msdn.microsoft.com/windows/apps/br229516.aspx) las obtengan.

La herramienta de MakeAppx.exe se encuentra normalmente en estas ubicaciones:

-   En x86: C: \\ archivos de programa (x86) \\ kits de Windows \\ 8,0 \\ bin \\ x86 \\makeappx.exe o C: \\ archivos de programa (x86) \\ kits de Windows \\ 8,1 \\ bin \\ x86 \\makeappx.exe
-   En x64 en dos ubicaciones:
    -   C: \\ archivos de programa (x86) \\ kits \\ de Windows 8,0 \\ bin \\ x86 \\makeappx.exe o C: \\ archivos de programa (x86) \\ kits de Windows \\ 8,1 \\ bin \\ x86 \\makeappx.exe
    -   C: \\ archivos de programa (x86) \\ kits \\ de Windows 8,0 \\ bin \\ x64 \\makeappx.exe o C: \\ archivos de programa (x86) \\ kits de Windows \\ 8,1 \\ bin \\ x64 \\makeappx.exe

No hay ninguna versión ARM de la herramienta.

-   [Para crear un paquete con una estructura de directorios](#to-create-a-package-using-a-directory-structure)
-   [Para crear un paquete mediante un archivo de asignación](#to-create-a-package-using-a-mapping-file)
-   [Para firmar el paquete con SignTool](#to-sign-the-package-using-signtool)
-   [Para extraer archivos de un paquete](#to-extract-files-from-a-package)
-   [Para crear una agrupación de paquetes mediante una estructura de directorios](#to-create-a-package-bundle-using-a-directory-structure)
-   [Para crear una agrupación de paquetes mediante un archivo de asignación](#to-create-a-package-bundle-using-a-mapping-file)
-   [Para extraer paquetes de un paquete](#to-extract-packages-from-a-bundle)
-   [Para cifrar un paquete con un archivo de clave](#to-encrypt-a-package-with-a-key-file)
-   [Para cifrar un paquete con una clave de prueba global](#to-encrypt-a-package-with-a-global-test-key)
-   [Para descifrar un paquete con un archivo de claves](#to-decrypt-a-package-with-a-key-file)
-   [Para descifrar un paquete con una clave de prueba global](#to-decrypt-a-package-with-a-global-test-key)
-   [Uso](#usage)

## <a name="using-app-packager"></a>Usar el Empaquetador de aplicaciones

> [!Note]  
> Las rutas de acceso relativas se admiten en toda la herramienta.

 

### <a name="to-create-a-package-using-a-directory-structure"></a>Para crear un paquete con una estructura de directorios

Coloque el AppxManifest.xml en la raíz de un directorio que contenga todos los archivos de carga de la aplicación. Se crea una estructura de directorio idéntica para el paquete de la aplicación y estará disponible cuando el paquete se extraiga en el momento de la implementación.

1.  Coloque todos los archivos en una única estructura de directorios y cree subdirectorios según sea necesario.

2.  Cree un manifiesto de paquete válido, AppxManifest.xml y colóquelo en el directorio raíz.

3.  Ejecute este comando:

    **Paquete de MakeAppx/d** *entrada \_ directoryPath* **/p** _filePath_**. appx**

### <a name="to-create-a-package-using-a-mapping-file"></a>Para crear un paquete mediante un archivo de asignación

1.  Cree un manifiesto de paquete válido AppxManifest.xml.

2.  Cree un archivo de asignación. La primera línea contiene los **\[ archivos \]** de cadena y las líneas siguientes especifican las rutas de acceso de origen (disco) y de destino (paquete) en cadenas entre comillas.

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  Ejecute este comando:

    **Paquete de MakeAppx/f** *asignando \_ filePath* **/p** _filePath_**. appx**

### <a name="to-sign-the-package-using-signtool"></a>Para firmar el paquete con SignTool

1.  Crea el certificado. El publicador que se muestra en el manifiesto debe coincidir con la información de asunto del publicador del certificado de firma. Para obtener más información sobre cómo crear un certificado de firma, consulte [Cómo crear un certificado de firma de paquete de aplicación](how-to-create-a-package-signing-certificate.md).

2.  Ejecute SignTool.exe para firmar el paquete:

    **SignTool Sign/a/v/FD**   *nombrearchivocertificado* _filePath_**. appx**

    El *hashAlgorithm* debe coincidir con el algoritmo hash usado para crear el blockmap cuando la aplicación se ha empaquetado. Con la utilidad de empaquetado de MakeAppx, el algoritmo hash blockmap de appx predeterminado es **SHA256**. Ejecute SignTool.exe especificando **SHA256** como el algoritmo de síntesis de archivo (/FD):

    **SignTool signo/a/v/FD** *nombrearchivocertificado* _filePath_**. appx**

    Para obtener más información sobre cómo firmar paquetes, consulte [cómo firmar un paquete de aplicación mediante SignTool](how-to-sign-a-package-using-signtool.md).

### <a name="to-extract-files-from-a-package"></a>Para extraer archivos de un paquete

1.  Ejecute este comando:

    **MakeAppx unpack/p** _File_**. appx/d** *\_ Directorio de salida*

2.  El paquete desempaquetado tiene la misma estructura que el paquete instalado.

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a>Para crear una agrupación de paquetes mediante una estructura de directorios

Usamos el comando de **agrupación** para crear un lote de aplicaciones en <output bundle name> agregando todos los paquetes de <content directory> (incluidas las subcarpetas). Si <content directory> contiene un manifiesto de agrupación, AppxBundleManifest.xml, se omite.

1.  Coloque todos los paquetes en una única estructura de directorios y cree subdirectorios según sea necesario.

2.  Ejecute este comando:

    **Paquete de MakeAppx/d** *entrada \_ directoryPath* **/p** _filePath_**. appxbundle**

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a>Para crear una agrupación de paquetes mediante un archivo de asignación

Usamos el comando de **agrupación** para crear un lote de aplicaciones en <output bundle name> agregando todos los paquetes de una lista de paquetes dentro de <mapping file> . Si <mapping file> contiene un manifiesto de agrupación, AppxBundleManifest.xml, se omite.

1.  Creará un control <mapping file>. La primera línea contiene los **\[ archivos \]** de cadena y las líneas siguientes especifican los paquetes que se van a agregar a la agrupación. Cada paquete se describe mediante un par de rutas de acceso entre comillas, separadas por espacios o tabulaciones. El par de rutas de acceso representa el origen del paquete (en disco) y el destino (en la agrupación). Todos los nombres de paquetes de destino deben tener la extensión. appx.

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  Ejecute este comando:

    **Paquete de MakeAppx** : *asignación de \_ filePath* **/p** _filePath_**. appxbundle**

### <a name="to-extract-packages-from-a-bundle"></a>Para extraer paquetes de un paquete

1.  Ejecute este comando:

    **Desagrupación de MakeAppx/p** _\_ nombre de lote_**. appxbundle/d** *\_ Directorio de salida*

2.  La agrupación desempaquetada tiene la misma estructura que el paquete de paquetes instalado.

### <a name="to-encrypt-a-package-with-a-key-file"></a>Para cifrar un paquete con un archivo de clave

1.  Cree un archivo de clave. Los archivos de clave deben comenzar con una línea que contenga la cadena " \[ Keys \] " seguida de las líneas que describen las claves con las que se va a cifrar el paquete. Cada clave se describe mediante un par de cadenas entre comillas, separadas por espacios o tabulaciones. La primera cadena representa el identificador de clave y la segunda cadena representa la clave de cifrado en formato hexadecimal.

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  Ejecute este comando:

    **MakeAppx.exe cifrar/p** _\_ nombre del paquete_**. appx/EP** _cifrado \_ \_ nombre del paquete_**. eappx/KF** _keyfile \_ nombre_**. txt**

3.  El paquete de entrada se cifrará en el paquete cifrado especificado mediante el archivo de clave proporcionado.

### <a name="to-encrypt-a-package-with-a-global-test-key"></a>Para cifrar un paquete con una clave de prueba global

1.  Ejecute este comando:

    **MakeAppx.exe cifrar/p** _\_ nombre del paquete_**. appx/EP** _\_ \_ nombre del paquete cifrado_**. eappx/KT**

2.  El paquete de entrada se cifrará en el paquete cifrado especificado mediante la clave de prueba global.

### <a name="to-decrypt-a-package-with-a-key-file"></a>Para descifrar un paquete con un archivo de claves

1.  Cree un archivo de clave. Los archivos de clave deben comenzar con una línea que contenga la cadena " \[ Keys \] " seguida de las líneas que describen las claves con las que se va a cifrar el paquete. Cada clave se describe mediante un par de cadenas entre comillas, separadas por espacios o tabulaciones. La primera cadena representa el identificador de clave de 32 bytes codificado en Base64 y la segunda cadena representa la clave de cifrado de 32 bytes codificada en Base64.

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  Ejecute este comando:

    **MakeAppx.exe descifrar/p** _\_ nombre del paquete_**. appx/EP no** _cifrado \_ \_ nombre del paquete_**. eappx/KF** _keyfile \_ nombre_**. txt**

3.  El paquete de entrada se descifrará en el paquete no cifrado especificado mediante el archivo de clave proporcionado.

### <a name="to-decrypt-a-package-with-a-global-test-key"></a>Para descifrar un paquete con una clave de prueba global

1.  Ejecute este comando:

    **MakeAppx.exe descifrar/p** _\_ nombre del paquete_**. appx/EP** _\_ \_ nombre del paquete sin cifrar_**. eappx/KT**

2.  El paquete de entrada se descifrará en el paquete no cifrado especificado con la clave de prueba global.

## <a name="usage"></a>Uso

El argumento de línea de comandos **/p** siempre es necesario, con **/d**, **/f** o **/EP**. Tenga en cuenta que **/d**, **/f** y **/EP** son mutuamente excluyentes.

**\[ Opciones \] del paquete de MakeAppx** **/p** *\<output package name\>* **/d***\<content directory\>*

**\[ Opciones \] del paquete de MakeAppx** **/p** *\<output package name\>* **/f***\<mapping file\>*

**\[ Opciones \] de desempaquetado de MakeAppx** **/p** *\<input package name\>* **/d***\<output directory\>*

**\[ Opciones \] de agrupación de MakeAppx** **/p** *\<output bundle name\>* **/d***\<content directory\>*

**\[ Opciones \] de agrupación de MakeAppx** **/p** *\<output bundle name\>* **/f***\<mapping file\>*

**\[ Opciones \] de desagrupación de MakeAppx** **/p** *\<input bundle name\>* **/d***\<output directory\>*

**\[ Opciones \] de cifrado de MakeAppx** **/p** *\<input package name\>* **/EP***\<output package name\>*

**\[ Opciones \] de descifrado de MakeAppx** **/p** *\<input package name\>* **/EP***\<output package name\>*

## <a name="command-line-syntax"></a>Sintaxis de línea de comandos

Esta es la sintaxis de uso común de línea de comandos para MakeAppx.

Paquete de MakeAppx desempaquetar agrupación desempaquetar **\[ \| \| \| \| cifrar cifrar el \| descifrado \]** \[ **/h** **/KF** **/KT** **/l** **/o** **/no** **/NV** **/v** **/pfn** **/?**\]

Los paquetes de **MakeAppx** o desempaquetan los archivos de un paquete, empaquetan o desempaquetan los paquetes de una agrupación, o cifran o descifran el paquete o el lote de la aplicación en el directorio de entrada o archivo de asignación especificado. Esta es la lista de parámetros que se aplican al **paquete de makeappx**, **desempaquetamiento de makeappx**, paquete de **makeappx**, **desagrupación de makeappx**, **cifrado** de makeappx o **descifrado de makeappx**.

<dl> <dt>

<span id="_l"></span><span id="_L"></span>**l**
</dt> <dd>

Esta opción se usa para los paquetes localizados. La validación predeterminados se desactiva en paquetes localizados. Esta opción deshabilita solo esa validación específica, sin requerir que se deshabilite toda la validación.

</dd> <dt>

<span id="_o"></span><span id="_O"></span>**/o**
</dt> <dd>

Sobrescriba el archivo de salida si existe. Si no se especifica esta opción o la opción **/no** , se pregunta al usuario si desea sobrescribir el archivo.

No se puede usar esta opción con **/no**.

</dd> <dt>

<span id="_no"></span><span id="_NO"></span>**/no**
</dt> <dd>

Se impide que se sobrescriba el archivo de salida, si lo hay. Si no se especifica esta opción o la opción **/o** , se pregunta al usuario si desea sobrescribir el archivo.

No puede usar esta opción con **/o**.

</dd> <dt>

<span id="_nv"></span><span id="_NV"></span>**/nv**
</dt> <dd>

Omitir la validación semántica. Si no se especifica esta opción, la herramienta realiza una validación completa del paquete.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Habilite la salida del registro detallado en la consola.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Mostrar texto de ayuda.

</dd> </dl>

**El paquete de makeappx** , el desempaquetado de **makeappx** , el paquete de **makeappx**, el **desempaquetado** de makeappx, el **cifrado de makeappx** y el **descifrado de makeappx** son comandos mutuamente exclusivos. Estos son los parámetros de línea de comandos que se aplican específicamente a cada comando:

**Paquete** \[ de MakeAppx **h**\]

Crea un paquete.

<dl> <dt>

<span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span> *algoritmo* /h
</dt> <dd>

Especifica el algoritmo hash que usar al crear la asignación de bloques. Estos son los valores válidos para el *algoritmo*:

<dl> <dd>SHA256 (predeterminado)</dd> <dd>SHA384</dd> <dd>SHA512</dd> </dl>

No puede usar esta opción con el comando **unpack** .

</dd> </dl>

**Desempaquetar MakeAppx** \[ **pfn**\]

Extrae todos los archivos del paquete especificado en el directorio de salida especificado. La salida tiene la misma estructura de directorios que el paquete.

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

Especifica un directorio denominado con el nombre completo del paquete. Este directorio se crea en la ubicación de salida proporcionada. No puede usar esta opción con el comando **Pack** .

</dd> </dl>

**Desagrupación** \[ de MakeAppx **pfn**\]

Desempaqueta todos los paquetes en un subdirectorio de la ruta de acceso de salida especificada, con el nombre completo del paquete. La salida tiene la misma estructura de directorios que el paquete de paquetes instalado.

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

Especifica un directorio denominado con el nombre completo de la agrupación de paquetes. Este directorio se crea en la ubicación de salida proporcionada. No se puede usar esta opción con el comando **bundle** .

</dd> </dl>

**Cifrado** \[ de MakeAppx **KF**, **KT**\]

Crea un paquete de aplicación cifrada a partir del paquete de la aplicación de entrada especificado en el paquete de salida especificado.

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/KF***<key file>*
</dt> <dd>

Cifra el paquete o agrupación utilizando la clave del archivo de clave especificado. Esta opción no se puede usar con **KT**.

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

Cifra el paquete o agrupación mediante la clave de prueba global. Esta opción no se puede usar con **KF**.

</dd> </dl>

**Descifrado** \[ de MakeAppx **KF**, **KT**\]

Crea un paquete de aplicación sin cifrar a partir del paquete de la aplicación de entrada especificado en el paquete de salida especificado.

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/KF***<key file>*
</dt> <dd>

Descifra el paquete o agrupación utilizando la clave del archivo de clave especificado. Esta opción no se puede usar con **KT**.

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

Descifra el paquete o agrupación mediante la clave de prueba global. Esta opción no se puede usar con **KF**.

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a>Validación semántica realizada por MakeAppx

MakeAppx realiza una validación semántica limitada que está diseñada para detectar los errores de implementación más comunes y ayudar a garantizar que el paquete de la aplicación es válido.

Esta validación garantiza que:

-   Todos los archivos a los que se hace referencia en el manifiesto del paquete se incluyen en el paquete de la aplicación.
-   Una aplicación no tiene dos claves idénticas.
-   Una aplicación no se registra para un protocolo prohibido en esta lista: SMB, archivo, MS-WWA-WEB, MS-WWA.

Esta validación semántica no está completa y no se garantiza que los paquetes compilados por MakeAppx sean instalables.

 

 
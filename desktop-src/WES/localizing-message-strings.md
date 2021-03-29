---
title: Localizar cadenas de mensaje
description: Cada cadena de mensaje que especifique en el manifiesto debe hacer referencia a una cadena en la sección de localización del manifiesto.
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7812aed8bf376994a2cbecfa5997737d9740ec1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078053"
---
# <a name="localizing-message-strings"></a><span data-ttu-id="843b6-103">Localizar cadenas de mensaje</span><span class="sxs-lookup"><span data-stu-id="843b6-103">Localizing Message Strings</span></span>

<span data-ttu-id="843b6-104">Cada cadena de mensaje que especifique en el manifiesto debe hacer referencia a una cadena en la sección de **localización** del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="843b6-104">Each message string that you specify in the manifest must reference a string in the **localization** section of the manifest.</span></span> <span data-ttu-id="843b6-105">La sección de localización contiene una sección de tabla de cadenas para cada configuración regional que admita.</span><span class="sxs-lookup"><span data-stu-id="843b6-105">The localization section contains a string table section for each locale that you support.</span></span>

<span data-ttu-id="843b6-106">En el ejemplo siguiente se muestra cómo definir una tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="843b6-106">The following example shows how to define a string table.</span></span> <span data-ttu-id="843b6-107">Debe especificar los atributos de **identificador** y **valor** de la cadena.</span><span class="sxs-lookup"><span data-stu-id="843b6-107">You must specify the string's **id** and **value** attributes.</span></span> <span data-ttu-id="843b6-108">El valor del atributo **ID** se usa para hacer referencia a la cadena en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="843b6-108">You use the value of the **id** attribute to reference the string in your manifest.</span></span> <span data-ttu-id="843b6-109">El atributo **Value** contiene la cadena localizada.</span><span class="sxs-lookup"><span data-stu-id="843b6-109">The **value** attribute contains the localized string.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider" 
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}" 
                symbol="PROVIDER_GUID" 
                resourceFileName="<path to the exe or dll that contains the metadata resources>" 
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.ProviderName)">

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="ProviderName" value="Sample Provider"/>
                <string id="PathNotFound" value="The path %1 was not found."/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```


<span data-ttu-id="843b6-110">En lugar de agregar cadenas traducidas al manifiesto, debe crear un archivo de interfaz de usuario multilingüe (MUI) para cada idioma admitido.</span><span class="sxs-lookup"><span data-stu-id="843b6-110">Instead of adding localized strings to the manifest, you should create a multilingual user interface (MUI) file for each language that you support.</span></span> <span data-ttu-id="843b6-111">Use un archivo de texto de mensaje para especificar las cadenas localizadas.</span><span class="sxs-lookup"><span data-stu-id="843b6-111">Use a message text file to specify your localized strings.</span></span>

<span data-ttu-id="843b6-112">En el procedimiento siguiente se describe cómo crear un archivo MUI para inglés y francés.</span><span class="sxs-lookup"><span data-stu-id="843b6-112">The following procedure describes how to create a MUI file for English and French.</span></span>

<span data-ttu-id="843b6-113">**Para crear un archivo MUI para inglés y francés**</span><span class="sxs-lookup"><span data-stu-id="843b6-113">**To create a MUI file for English and French**</span></span>

1.  <span data-ttu-id="843b6-114">Cree un archivo de texto de mensaje que cree las cadenas de mensajes en francés.</span><span class="sxs-lookup"><span data-stu-id="843b6-114">Create a message text file that creates the French message strings.</span></span> <span data-ttu-id="843b6-115">Para obtener más información sobre cómo crear un archivo de texto de mensaje, vea [archivos de texto de mensaje](/windows/desktop/EventLog/message-text-files).</span><span class="sxs-lookup"><span data-stu-id="843b6-115">For details on creating a message text file, see [Message Text Files](/windows/desktop/EventLog/message-text-files).</span></span> <span data-ttu-id="843b6-116">Los identificadores de mensaje que se especifiquen en el archivo de texto del mensaje deben coincidir con los identificadores de recursos generados por el compilador de mensajes para las mismas cadenas del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="843b6-116">The message identifiers that you specify in the message text file must match the resource identifiers that the message compiler generated for the same strings in the manifest.</span></span> <span data-ttu-id="843b6-117">Para determinar los identificadores de recursos usados para las cadenas del manifiesto, vea el archivo. h que el compilador de mensajes generó al compilar el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="843b6-117">To determine the resource identifiers used for the strings in the manifest, see the .h file that the message compiler generated when you compiled the manifest.</span></span>
    ```Text
    LanguageNames=(French=0x40C:MSG0040C)

    ; // The following are message definitions.

    MessageId=0x00000065
    SymbolicName=MSG_ProviderName
    Language=French
    <FRENCH STRING GOES HERE>
    .


    MessageId=0x00000066
    SymbolicName=MSG_PathNotFound
    Language=French
    <FRENCH STRING GOES HERE>
    .
    
    ```


2.  <span data-ttu-id="843b6-118">Ejecute los siguientes comandos para crear el archivo DLL de recursos que contiene las cadenas localizadas.</span><span class="sxs-lookup"><span data-stu-id="843b6-118">Run the following commands to create the resource DLL that contains your localized strings.</span></span> <span data-ttu-id="843b6-119">El archivo messages.mc es el archivo de texto del mensaje que creó en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="843b6-119">The messages.mc file is the message text file that you created in step 1.</span></span>
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  <span data-ttu-id="843b6-120">En la carpeta que contiene el proveedor, cree una subcarpeta para cada configuración regional que admita.</span><span class="sxs-lookup"><span data-stu-id="843b6-120">In the folder that contains your provider, create a subfolder for each locale that you support.</span></span> <span data-ttu-id="843b6-121">El nombre de la subcarpeta debe ser el nombre de idioma de esa configuración regional.</span><span class="sxs-lookup"><span data-stu-id="843b6-121">The name of the subfolder must be the language name for that locale.</span></span> <span data-ttu-id="843b6-122">Por ejemplo, para 0x0409, use en-US como nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="843b6-122">For example, for 0x0409, use en-US as the folder name.</span></span>
4.  <span data-ttu-id="843b6-123">Cree un archivo. rcconfig que indique a la herramienta Muirct.exe que desea dividir los recursos de cadena de mensaje del archivo ejecutable y los archivos dll de recursos.</span><span class="sxs-lookup"><span data-stu-id="843b6-123">Create a .rcconfig file that tells the Muirct.exe tool that you want to split the message string resources from the executable and the resource DLLs.</span></span> <span data-ttu-id="843b6-124">A continuación se encuentra un archivo. rcconfig de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="843b6-124">The following is an example .rcconfig file.</span></span>
    ```XML
    <localization>
          <resources>
                <win32Resources fileType="Application">
                      <neutralResources>
                      </neutralResources>
                      <localizedResources>
                            <resourceType typeNameId="#11"/>
                      </localizedResources>
                </win32Resources>
          </resources>
    </localization>
    ```
  

5.  <span data-ttu-id="843b6-125">Ejecute los siguientes comandos de Muirct.exe para dividir las cadenas en inglés del archivo ejecutable del proveedor.</span><span class="sxs-lookup"><span data-stu-id="843b6-125">Run the following Muirct.exe commands to split the English strings from the provider executable file.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  <span data-ttu-id="843b6-126">Ejecute los siguientes comandos de Muirct.exe para dividir las cadenas de francés del archivo DLL de recursos.</span><span class="sxs-lookup"><span data-stu-id="843b6-126">Run the following Muirct.exe commands to split the French strings from the resource DLL.</span></span> <span data-ttu-id="843b6-127">Quite el archivo neutro de idioma (fr-FR \\messages.dll) una vez creado el archivo MUI.</span><span class="sxs-lookup"><span data-stu-id="843b6-127">Remove the language neutral file (fr-FR\\messages.dll) after the MUI file is created.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  <span data-ttu-id="843b6-128">Cambie el nombre de provider.exe. LN a provider.exe.</span><span class="sxs-lookup"><span data-stu-id="843b6-128">Rename provider.exe.ln to provider.exe.</span></span>
---
title: Localización de cadenas de mensaje
description: Cada cadena de mensaje que especifique en el manifiesto debe hacer referencia a una cadena en la sección de localización del manifiesto.
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55b94ea8e8a40de1401cf3aba97488d5531a77b441361e38f1ff98219940afc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587903"
---
# <a name="localizing-message-strings"></a>Localización de cadenas de mensaje

Cada cadena de mensaje que especifique en el manifiesto debe hacer referencia a una cadena en la **sección de localización** del manifiesto. La sección de localización contiene una sección de tabla de cadenas para cada configuración regional que admita.

En el ejemplo siguiente se muestra cómo definir una tabla de cadenas. Debe especificar los atributos id **y** value de **la** cadena. Use el valor del atributo **id** para hacer referencia a la cadena en el manifiesto. El **atributo value** contiene la cadena localizada.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
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


En lugar de agregar cadenas localizadas al manifiesto, debe crear un archivo de interfaz de usuario multilingüe (MUI) para cada idioma que admita. Use un archivo de texto de mensaje para especificar las cadenas localizadas.

En el procedimiento siguiente se describe cómo crear un archivo CSV para inglés y francés.

**Para crear un archivo MUI para inglés y francés**

1.  Cree un archivo de texto de mensaje que cree las cadenas de mensaje en francés. Para obtener más información sobre cómo crear un archivo de texto de mensaje, vea [Archivos de texto de mensaje](/windows/desktop/EventLog/message-text-files). Los identificadores de mensaje que especifique en el archivo de texto del mensaje deben coincidir con los identificadores de recursos que el compilador de mensajes generó para las mismas cadenas en el manifiesto. Para determinar los identificadores de recursos usados para las cadenas del manifiesto, vea el archivo .h que el compilador de mensajes generó al compilar el manifiesto.
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


2.  Ejecute los siguientes comandos para crear el archivo DLL de recursos que contiene las cadenas localizadas. El messages.mc es el archivo de texto de mensaje que creó en el paso 1.
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  En la carpeta que contiene el proveedor, cree una subcarpeta para cada configuración regional que admita. El nombre de la subcarpeta debe ser el nombre de idioma de esa configuración regional. Por ejemplo, para 0x0409, use en-US como nombre de la carpeta.
4.  Cree un archivo .rcconfig que indique a la Muirct.exe que desea dividir los recursos de cadena de mensaje del archivo ejecutable y los archivos DLL de recursos. A continuación se muestra un archivo .rcconfig de ejemplo.
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
  

5.  Ejecute los siguientes Muirct.exe comandos para dividir las cadenas en inglés del archivo ejecutable del proveedor.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  Ejecute los siguientes Muirct.exe comandos para dividir las cadenas en francés del archivo DLL de recursos. Quite el archivo neutro del idioma (fr-FR \\messages.dll) después de crear el archivo DE LAA.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  Cambie provider.exe.ln a provider.exe.

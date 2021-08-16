---
title: Load (Método)
description: Load (Método)
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e201053bf3eb9fbd7a3c5c7eb94f9b032cde13087f76e1fcfa176d068655137a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748665"
---
# <a name="load-method"></a>Load (Método)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Carga un carácter en la [**colección**](/windows/desktop/lwef/the-characters-object) Caracteres.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Characters.Load "**_CharacterID_*_",_ *  *Provider*



| Parte          | Descripción                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Obligatorio. Valor de cadena que usará para hacer referencia a los datos de caracteres que se van a cargar.                                                                                                                                                  |
| *Proveedor*    | Obligatorio. Tipo de datos variant que debe ser uno de los siguientes: **Filespec** La ubicación del archivo de definición del carácter especificado. <br/> **DIRECCIÓN URL** Dirección HTTP del archivo de definición del carácter.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede cargar caracteres desde el subdirectorio Del Agente especificando una ruta de acceso relativa (una que no incluya dos puntos ni un carácter de barra diagonal inicial). Esto prefida la ruta de acceso con el directorio de caracteres del agente (ubicado en el directorio Windows \\ msagent). Por ejemplo, si se especifica lo siguiente, se cargaría Genie.acs desde el directorio Chars del agente:


```
   Agent.Character.Load "genie", "genie.acs"
```



También puede especificar su propio directorio en el directorio Chars del agente.


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



Puede cargar el carácter establecido actualmente como el carácter predeterminado del usuario actual sin incluir una ruta de acceso como segundo parámetro del **método Load.**


```
   Agent.Character.Load "character"
```



No se puede cargar el mismo carácter (un carácter con el mismo GUID) más de una vez desde una sola instancia del control. Del mismo modo, no puede cargar el carácter predeterminado y otros caracteres al mismo tiempo desde una sola instancia del control porque el carácter predeterminado podría ser el mismo que el otro carácter. Si intenta hacerlo, el servidor genera un error. Sin embargo, puede crear otra instancia del control Agente y cargar el mismo carácter.

El proveedor de datos de Microsoft Agent admite la carga de datos de caracteres almacenados como un único archivo estructurado (. ACS) con datos de caracteres y datos de animación juntos o como datos de caracteres independientes (. ACF) y animación (. ACA). Use la estructura única . Archivo de ACS para cargar un carácter que se almacena en un disco o red local y al que se accede mediante un protocolo de archivo convencional (por ejemplo, unC pathnames). Use el independiente . ACF y . Archivos ACA cuando quiera cargar los archivos de animación individualmente desde un sitio remoto al que se accede mediante el protocolo HTTP.

Para. Los archivos de ACS, mediante **el método Load** proporcionan acceso a las animaciones de un carácter. Para. Archivos ACF, también se usa el [**método Get**](get-method.md) para cargar datos de animación. El **método Load** no admite la descarga de . Archivos de ACS desde un sitio HTTP.

La carga de un carácter no muestra automáticamente el carácter. Use primero [**el método Show**](show-method.md) para que el carácter sea visible.

Si usa el método **Load** para cargar un archivo de caracteres almacenado en la máquina local y se produce un error en la llamada; Por ejemplo, como no se encuentra el archivo, el Agente genera un error. Puede usar la compatibilidad en el lenguaje de programación para proporcionar una rutina de control de errores para detectar y procesar el error.


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



También puede controlar el error si establece [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) en **False,** declara un objeto y le asigna la **solicitud Load.** A continuación, **siga la llamada** a Load con una instrucción que comprueba el estado del objeto [**Request.**](/windows/desktop/lwef/the-request-object)


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



Si carga un carácter que no es local; Por ejemplo, mediante el protocolo HTTP,  también puede comprobar si hay un error de carga asignando un objeto [**Request**](/windows/desktop/lwef/the-request-object) al **método Load.** Sin embargo, dado que este método de carga de un carácter se controla de forma asincrónica, compruebe su estado en el [**evento RequestComplete.**](requestcomplete-event.md) Esta técnica no funcionará cargando un carácter mediante el protocolo UNC porque el **método Load** se procesa sincrónicamente.

 


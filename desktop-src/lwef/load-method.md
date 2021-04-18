---
title: Load (Método)
description: Load (Método)
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927fc8e49e55c2bdfcd7b1109bb8604540c199c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704949"
---
# <a name="load-method"></a>Load (Método)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Carga un carácter en la colección de [**caracteres**](/windows/desktop/lwef/the-characters-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres. Load "*** CharacterID * *",* *  *proveedor*



| Parte          | Descripción                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Obligatorio. Valor de cadena que se va a utilizar para hacer referencia a los datos de caracteres que se van a cargar.                                                                                                                                                  |
| *Proveedor*    | Obligatorio. Un tipo de datos Variant que debe ser uno de los siguientes: **filespec** la ubicación del archivo local del archivo de definición del carácter especificado. <br/> **Dirección URL** Dirección HTTP del archivo de definición del carácter.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede cargar caracteres del subdirectorio del agente especificando una ruta de acceso relativa (una que no incluya un carácter de dos puntos o una barra diagonal inicial). Esto antepone la ruta de acceso con el directorio de caracteres del agente (ubicado en el \\ directorio MSAgent de Windows localizado). Por ejemplo, al especificar lo siguiente se cargará el genio. ACS del directorio chars del agente:


```
   Agent.Character.Load "genie", "genie.acs"
```



También puede especificar su propio directorio en el directorio chars del agente.


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



Puede cargar el carácter establecido actualmente como el carácter predeterminado del usuario actual sin incluir una ruta de acceso como segundo parámetro del método **Load** .


```
   Agent.Character.Load "character"
```



No se puede cargar el mismo carácter (un carácter que tiene el mismo GUID) más de una vez desde una única instancia del control. Del mismo modo, no se puede cargar el carácter predeterminado y otros caracteres al mismo tiempo desde una única instancia del control, ya que el carácter predeterminado podría ser el mismo que el otro carácter. Si intenta hacerlo, el servidor genera un error. Sin embargo, puede crear otra instancia del control del agente y cargar el mismo carácter.

El proveedor de datos del agente de Microsoft admite la carga de datos de caracteres almacenados como un solo archivo estructurado (. ACS) con datos de caracteres y de animación juntos o como datos de caracteres independientes (. ACF) y animación (. ACA). Use la estructura única. Archivo de ACS para cargar un carácter que está almacenado en un disco local o en una red y a la que se tiene acceso mediante un protocolo de archivo convencional (por ejemplo, rutas de acceso UNC). Use la independiente. ACF y. Los archivos ACA cuando desea cargar los archivos de animación de forma individual desde un sitio remoto al que se tiene acceso mediante el protocolo HTTP.

Para. Los archivos de ACS, mediante el método **Load** , proporcionan acceso a las animaciones de un carácter. Para. Archivos ACF, también se usa el método [**Get**](get-method.md) para cargar los datos de animación. El método **Load** no admite la descarga. Archivos de ACS de un sitio HTTP.

Al cargar un carácter, no se muestra automáticamente el carácter. Use el método [**Show**](show-method.md) primero para que el carácter esté visible.

Si usa el método **Load** para cargar un archivo de caracteres almacenado en el equipo local y se produce un error en la llamada; por ejemplo, como no se encuentra el archivo, el agente genera un error. Puede usar la compatibilidad en el lenguaje de programación para proporcionar una rutina de control de errores para detectar y procesar el error.


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



También puede controlar el error si establece [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) en **false**, declara un objeto y le asigna la solicitud de **carga** . Después, siga la llamada de **carga** con una instrucción que comprueba el estado del objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .


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



Si carga un carácter que no es local; por ejemplo, mediante el protocolo HTTP, también puede comprobar si hay un error de **carga** mediante la asignación de un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) al método **Load** . Sin embargo, dado que este método de carga de un carácter se controla de forma asincrónica, compruebe su estado en el evento [**RequestComplete**](requestcomplete-event.md) . Esta técnica no funcionará al cargar un carácter mediante el protocolo UNC, ya que el método **Load** se procesa de forma sincrónica.

 


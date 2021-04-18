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
# <a name="load-method"></a><span data-ttu-id="5036d-103">Load (Método)</span><span class="sxs-lookup"><span data-stu-id="5036d-103">Load Method</span></span>

<span data-ttu-id="5036d-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5036d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5036d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="5036d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5036d-106">Carga un carácter en la colección de [**caracteres**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="5036d-106">Loads a character into the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="5036d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="5036d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5036d-108">\*agente ***. Caracteres. Load "*** CharacterID \* *",* \*  *proveedor*</span><span class="sxs-lookup"><span data-stu-id="5036d-108">*agent ***.Characters.Load "*** CharacterID\*\*\*",*\* *Provider*</span></span>



| <span data-ttu-id="5036d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="5036d-109">Part</span></span>          | <span data-ttu-id="5036d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5036d-110">Description</span></span>                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5036d-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="5036d-111">*CharacterID*</span></span> | <span data-ttu-id="5036d-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5036d-112">Required.</span></span> <span data-ttu-id="5036d-113">Valor de cadena que se va a utilizar para hacer referencia a los datos de caracteres que se van a cargar.</span><span class="sxs-lookup"><span data-stu-id="5036d-113">A string value that you will use to refer to the character data to be loaded.</span></span>                                                                                                                                                  |
| <span data-ttu-id="5036d-114">*Proveedor*</span><span class="sxs-lookup"><span data-stu-id="5036d-114">*Provider*</span></span>    | <span data-ttu-id="5036d-115">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5036d-115">Required.</span></span> <span data-ttu-id="5036d-116">Un tipo de datos Variant que debe ser uno de los siguientes: **filespec** la ubicación del archivo local del archivo de definición del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="5036d-116">A variant data type that must be one of the following: **Filespec** The local file location of the specified character's definition file.</span></span> <br/> <span data-ttu-id="5036d-117">**Dirección URL** Dirección HTTP del archivo de definición del carácter.</span><span class="sxs-lookup"><span data-stu-id="5036d-117">**URL** The HTTP address for the character's definition file.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5036d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5036d-118">Remarks</span></span>

<span data-ttu-id="5036d-119">Puede cargar caracteres del subdirectorio del agente especificando una ruta de acceso relativa (una que no incluya un carácter de dos puntos o una barra diagonal inicial).</span><span class="sxs-lookup"><span data-stu-id="5036d-119">You can load characters from the Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="5036d-120">Esto antepone la ruta de acceso con el directorio de caracteres del agente (ubicado en el \\ directorio MSAgent de Windows localizado).</span><span class="sxs-lookup"><span data-stu-id="5036d-120">This prefixes the path with Agent's characters directory (located in the localized Windows\\msagent directory).</span></span> <span data-ttu-id="5036d-121">Por ejemplo, al especificar lo siguiente se cargará el genio. ACS del directorio chars del agente:</span><span class="sxs-lookup"><span data-stu-id="5036d-121">For example, specifying the following would load Genie.acs from Agent's Chars directory:</span></span>


```
   Agent.Character.Load "genie", "genie.acs"
```



<span data-ttu-id="5036d-122">También puede especificar su propio directorio en el directorio chars del agente.</span><span class="sxs-lookup"><span data-stu-id="5036d-122">You can also specify your own directory in Agent's Chars directory.</span></span>


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



<span data-ttu-id="5036d-123">Puede cargar el carácter establecido actualmente como el carácter predeterminado del usuario actual sin incluir una ruta de acceso como segundo parámetro del método **Load** .</span><span class="sxs-lookup"><span data-stu-id="5036d-123">You can load the character currently set as the current user's default character by not including a path as the second parameter of the **Load** method.</span></span>


```
   Agent.Character.Load "character"
```



<span data-ttu-id="5036d-124">No se puede cargar el mismo carácter (un carácter que tiene el mismo GUID) más de una vez desde una única instancia del control.</span><span class="sxs-lookup"><span data-stu-id="5036d-124">You cannot load the same character (a character having the same GUID) more than once from a single instance of the control.</span></span> <span data-ttu-id="5036d-125">Del mismo modo, no se puede cargar el carácter predeterminado y otros caracteres al mismo tiempo desde una única instancia del control, ya que el carácter predeterminado podría ser el mismo que el otro carácter.</span><span class="sxs-lookup"><span data-stu-id="5036d-125">Similarly, you cannot load the default character and other characters at the same time from a single instance of the control because the default character could be the same as the other character.</span></span> <span data-ttu-id="5036d-126">Si intenta hacerlo, el servidor genera un error.</span><span class="sxs-lookup"><span data-stu-id="5036d-126">If you attempt to do this, the server raises an error.</span></span> <span data-ttu-id="5036d-127">Sin embargo, puede crear otra instancia del control del agente y cargar el mismo carácter.</span><span class="sxs-lookup"><span data-stu-id="5036d-127">However, you can create another instance of the Agent control and load the same character.</span></span>

<span data-ttu-id="5036d-128">El proveedor de datos del agente de Microsoft admite la carga de datos de caracteres almacenados como un solo archivo estructurado (. ACS) con datos de caracteres y de animación juntos o como datos de caracteres independientes (. ACF) y animación (. ACA).</span><span class="sxs-lookup"><span data-stu-id="5036d-128">The Microsoft Agent Data Provider supports loading character data stored either as a single structured file (.ACS) with character data and animation data together or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="5036d-129">Use la estructura única. Archivo de ACS para cargar un carácter que está almacenado en un disco local o en una red y a la que se tiene acceso mediante un protocolo de archivo convencional (por ejemplo, rutas de acceso UNC).</span><span class="sxs-lookup"><span data-stu-id="5036d-129">Use the single structured .ACS file to load a character that is stored on a local disk or network and accessed using a conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="5036d-130">Use la independiente. ACF y. Los archivos ACA cuando desea cargar los archivos de animación de forma individual desde un sitio remoto al que se tiene acceso mediante el protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="5036d-130">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using the HTTP protocol.</span></span>

<span data-ttu-id="5036d-131">Para. Los archivos de ACS, mediante el método **Load** , proporcionan acceso a las animaciones de un carácter.</span><span class="sxs-lookup"><span data-stu-id="5036d-131">For .ACS files, using the **Load** method provides access to a character's animations.</span></span> <span data-ttu-id="5036d-132">Para. Archivos ACF, también se usa el método [**Get**](get-method.md) para cargar los datos de animación.</span><span class="sxs-lookup"><span data-stu-id="5036d-132">For .ACF files, you also use the [**Get**](get-method.md) method to load animation data.</span></span> <span data-ttu-id="5036d-133">El método **Load** no admite la descarga. Archivos de ACS de un sitio HTTP.</span><span class="sxs-lookup"><span data-stu-id="5036d-133">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="5036d-134">Al cargar un carácter, no se muestra automáticamente el carácter.</span><span class="sxs-lookup"><span data-stu-id="5036d-134">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="5036d-135">Use el método [**Show**](show-method.md) primero para que el carácter esté visible.</span><span class="sxs-lookup"><span data-stu-id="5036d-135">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

<span data-ttu-id="5036d-136">Si usa el método **Load** para cargar un archivo de caracteres almacenado en el equipo local y se produce un error en la llamada; por ejemplo, como no se encuentra el archivo, el agente genera un error.</span><span class="sxs-lookup"><span data-stu-id="5036d-136">If you use the **Load** method to load a character file stored on the local machine and the call fails; for example, because the file is not found, Agent raises an error.</span></span> <span data-ttu-id="5036d-137">Puede usar la compatibilidad en el lenguaje de programación para proporcionar una rutina de control de errores para detectar y procesar el error.</span><span class="sxs-lookup"><span data-stu-id="5036d-137">You can use the support in your programming language to provide an error handling routine to catch and process the error.</span></span>


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



<span data-ttu-id="5036d-138">También puede controlar el error si establece [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) en **false**, declara un objeto y le asigna la solicitud de **carga** .</span><span class="sxs-lookup"><span data-stu-id="5036d-138">You can also handle the error by setting [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) to **False**, declaring a object, and assigning the **Load** request to it.</span></span> <span data-ttu-id="5036d-139">Después, siga la llamada de **carga** con una instrucción que comprueba el estado del objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="5036d-139">Then follow the **Load** call with a statement that checks the status of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>


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



<span data-ttu-id="5036d-140">Si carga un carácter que no es local; por ejemplo, mediante el protocolo HTTP, también puede comprobar si hay un error de **carga** mediante la asignación de un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) al método **Load** .</span><span class="sxs-lookup"><span data-stu-id="5036d-140">If you load a character that is not local; for example, using HTTP protocol, you can also check for a **Load** failure by assigning a [**Request**](/windows/desktop/lwef/the-request-object) object to the **Load** method.</span></span> <span data-ttu-id="5036d-141">Sin embargo, dado que este método de carga de un carácter se controla de forma asincrónica, compruebe su estado en el evento [**RequestComplete**](requestcomplete-event.md) .</span><span class="sxs-lookup"><span data-stu-id="5036d-141">However, because this method of loading a character is handled asynchronously, check its status in the [**RequestComplete**](requestcomplete-event.md) event.</span></span> <span data-ttu-id="5036d-142">Esta técnica no funcionará al cargar un carácter mediante el protocolo UNC, ya que el método **Load** se procesa de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="5036d-142">This technique will not work loading a character using the UNC protocol because the **Load** method is processed synchronously.</span></span>

 


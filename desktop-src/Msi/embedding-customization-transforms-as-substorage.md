---
description: Puede almacenar la transformación de personalización en un almacenamiento del paquete Windows Installer para garantizar que la transformación esté siempre disponible cuando el paquete de instalación esté disponible.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Incrustar transformaciones de personalización como subalmacenamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652750"
---
# <a name="embedding-customization-transforms-as-substorage"></a><span data-ttu-id="5b4e1-103">Incrustar transformaciones de personalización como subalmacenamiento</span><span class="sxs-lookup"><span data-stu-id="5b4e1-103">Embedding Customization Transforms as Substorage</span></span>

<span data-ttu-id="5b4e1-104">Puede almacenar la transformación de personalización en un almacenamiento del paquete Windows Installer para garantizar que la transformación esté siempre disponible cuando el paquete de instalación esté disponible.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-104">You may store the customization transform in a storage of the Windows Installer package to guarantee that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="5b4e1-105">Vea [transformaciones incrustadas](embedded-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="5b4e1-105">See [Embedded Transforms](embedded-transforms.md).</span></span> <span data-ttu-id="5b4e1-106">Un ejemplo de esto se proporciona en el SDK de Windows Installer como la utilidad WiSubStg.vbs.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-106">An example of this is provided in the Windows Installer SDK as the utility WiSubStg.vbs.</span></span> <span data-ttu-id="5b4e1-107">En el siguiente fragmento de código, Emb.vbs, también se muestra el uso de la [tabla Storages](-storages-table.md) para agregar una transformación incrustada que se usa con Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-107">The following snippet, Emb.vbs, also illustrates the use of the [Storages table](-storages-table.md) to add an embedded transform and is for use with Windows Script Host.</span></span>


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



<span data-ttu-id="5b4e1-108">Para agregar un almacenamiento llamado MNPtrans1 a MNP2000.msi y que contenga la transformación que creó en [Agregar información de resumen a la transformación de personalización](adding-summary-information-to-customization-transform.md), cambie los directorios a la carpeta que contiene Emb.vbs, la base de datos original y el archivo de transformación y, a continuación, escriba la siguiente línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-108">To add a storage named MNPtrans1 to MNP2000.msi, and containing the transform you created in [Adding Summary Information to Customization Transform](adding-summary-information-to-customization-transform.md), change directories to the folder containing Emb.vbs, the original database, and the transform file, then enter the following command line.</span></span>

<span data-ttu-id="5b4e1-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans. MST MNPtrans1**</span><span class="sxs-lookup"><span data-stu-id="5b4e1-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans.mst MNPtrans1**</span></span>

<span data-ttu-id="5b4e1-110">Esto completa el ejemplo de transformación de personalización.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-110">This completes the customization transform example.</span></span> <span data-ttu-id="5b4e1-111">Después de incrustar la transformación en MNPtrans. MST, la transformación siempre está disponible con el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-111">After embedding the transform in MNPtrans.mst, the transform is always available with the installation package.</span></span> <span data-ttu-id="5b4e1-112">No es necesario que el archivo MNPtrans. MST se encuentre en el origen para aplicar la transformación.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-112">The file MNPtrans.mst does not need to be located at the source to apply the transform.</span></span>

<span data-ttu-id="5b4e1-113">Quite MNPtrans. MST de la carpeta que contiene el paquete de instalación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-113">Remove MNPtrans.mst from the folder containing the sample installation package.</span></span> <span data-ttu-id="5b4e1-114">Haga clic en el icono de MNP2000.msi para iniciar una instalación o use la siguiente línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-114">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="5b4e1-115">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="5b4e1-115">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="5b4e1-116">Tenga en cuenta que esto instala el producto sin las personalizaciones.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-116">Note that this installs the product without the customizations.</span></span> <span data-ttu-id="5b4e1-117">Para instalar con las personalizaciones, escriba la siguiente línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-117">To install with the customizations, enter the following command line.</span></span> <span data-ttu-id="5b4e1-118">Use un signo de dos puntos para indicar que el valor de la propiedad [**TRANSformations**](transforms.md) hace referencia a una transformación incrustada.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-118">Use a colon to indicate that the value of the [**TRANSFORMS**](transforms.md) Property refers to an embedded transform.</span></span>

<span data-ttu-id="5b4e1-119">msiexec/i MNP2000.msi transformaciones =: MNPtrans1</span><span class="sxs-lookup"><span data-stu-id="5b4e1-119">msiexec /i MNP2000.msi TRANSFORMS=:MNPtrans1</span></span>

<span data-ttu-id="5b4e1-120">Tenga en cuenta que la característica de puerta no aparece en el árbol de selección de características y que los componentes de la característica de puerta no se instalan incluso si se selecciona un tipo de instalación completo en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5b4e1-120">Note that the Gate feature does not appear in the feature selection tree and that the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

## <a name="next-example"></a><span data-ttu-id="5b4e1-121">Ejemplo siguiente</span><span class="sxs-lookup"><span data-stu-id="5b4e1-121">Next example</span></span>

[<span data-ttu-id="5b4e1-122">Un pequeño ejemplo de revisión de actualización</span><span class="sxs-lookup"><span data-stu-id="5b4e1-122">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

 

 




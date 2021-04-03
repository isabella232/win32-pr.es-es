---
title: Libretas de teléfonos RAS
description: Las libretas de teléfonos proporcionan una manera estándar de recopilar y especificar la información que el administrador de conexiones de acceso remoto necesita para establecer una conexión remota.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Libretas de teléfonos, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075821"
---
# <a name="ras-phone-books"></a><span data-ttu-id="8ac32-104">Libretas de teléfonos RAS</span><span class="sxs-lookup"><span data-stu-id="8ac32-104">RAS Phone Books</span></span>

<span data-ttu-id="8ac32-105">Las libretas de teléfonos proporcionan una manera estándar de recopilar y especificar la información que el administrador de conexiones de acceso remoto necesita para establecer una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="8ac32-105">Phone books provide a standard way to collect and specify the information that the Remote Access Connection Manager needs to establish a remote connection.</span></span> <span data-ttu-id="8ac32-106">Las libretas de teléfonos asocian nombres de entradas a información como números de teléfono, puertos COM y configuraciones de módem.</span><span class="sxs-lookup"><span data-stu-id="8ac32-106">Phone books associate entry names with information such as phone numbers, COM ports, and modem settings.</span></span> <span data-ttu-id="8ac32-107">Cada entrada de libreta de teléfonos contiene la información necesaria para establecer una conexión RAS.</span><span class="sxs-lookup"><span data-stu-id="8ac32-107">Each phone-book entry contains the information needed to establish a RAS connection.</span></span>

<span data-ttu-id="8ac32-108">Las libretas de teléfonos se almacenan en archivos de libreta de teléfonos, que son archivos de texto que contienen los nombres de entrada y la información asociada.</span><span class="sxs-lookup"><span data-stu-id="8ac32-108">Phone books are stored in phone-book files, which are text files that contain the entry names and associated information.</span></span> <span data-ttu-id="8ac32-109">RAS crea un archivo de libreta de teléfonos denominado RASPHONE. PBK.</span><span class="sxs-lookup"><span data-stu-id="8ac32-109">RAS creates a phone-book file called RASPHONE.PBK.</span></span> <span data-ttu-id="8ac32-110">El usuario puede usar el cuadro de diálogo principal **redes de acceso telefónico** para crear archivos de libreta de teléfonos personales.</span><span class="sxs-lookup"><span data-stu-id="8ac32-110">The user can use the main **Dial-Up Networking** dialog box to create personal phone-book files.</span></span> <span data-ttu-id="8ac32-111">La API de RAS no es compatible actualmente con la creación de un archivo de libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="8ac32-111">The RAS API does not currently provide support for creating a phone-book file.</span></span> <span data-ttu-id="8ac32-112">Algunas funciones RAS, como la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , tienen un parámetro que especifica un archivo de libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="8ac32-112">Some RAS functions, such as the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function, have a parameter that specifies a phone-book file.</span></span> <span data-ttu-id="8ac32-113">Si el autor de la llamada no especifica un archivo de libreta de teléfonos, la función utiliza el archivo de libreta de teléfonos predeterminado, que es el seleccionado por el usuario en la hoja de propiedades **preferencias del usuario** del cuadro de diálogo **acceso telefónico a redes** .</span><span class="sxs-lookup"><span data-stu-id="8ac32-113">If the caller does not specify a phone-book file, the function uses the default phone-book file, which is the one selected by the user in the **User Preferences** property sheet of the **Dial-Up Networking** dialog box.</span></span>

<span data-ttu-id="8ac32-114">Windows NT 4,0 proporciona las funciones [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) y [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) que muestran la interfaz de usuario ras integrada que permite a los usuarios trabajar con las libretas de teléfonos y entradas de libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="8ac32-114">Windows NT 4.0 provides the [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) and [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) functions that display the built-in RAS user interface that enable users to work with phone books and phone-book entries.</span></span>

<span data-ttu-id="8ac32-115">**Windows 95:** Acceso telefónico a redes almacena entradas de libreta de teléfonos en el registro en lugar de en un archivo de libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="8ac32-115">**Windows 95:** Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.</span></span> <span data-ttu-id="8ac32-116">Windows 95 no admite archivos de libreta de teléfonos personales ni funciones que muestren los cuadros de diálogo de RAS integrados.</span><span class="sxs-lookup"><span data-stu-id="8ac32-116">Windows 95 does not support personal phone-book files or functions that display the built-in RAS dialog boxes.</span></span>

 

 





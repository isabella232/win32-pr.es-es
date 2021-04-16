---
title: Registro del complemento DVC
description: Describe la sintaxis de la entrada del complemento de canal virtual dinámico (DVC) del cliente Conexión a Escritorio remoto (RDC).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183c73f5f9dda0321640119b2750776d207973cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676471"
---
# <a name="dvc-plug-in-registration"></a><span data-ttu-id="b051f-103">Registro del complemento DVC</span><span class="sxs-lookup"><span data-stu-id="b051f-103">DVC plug-in registration</span></span>

<span data-ttu-id="b051f-104">El complemento de canal virtual dinámico (DVC) se registra para su uso por parte del cliente de Conexión a Escritorio remoto (RDC) mediante uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b051f-104">The dynamic virtual channel (DVC) plug-in is registered for use by the Remote Desktop Connection (RDC) client using one of the following methods:</span></span>

-   <span data-ttu-id="b051f-105">Invocar el método [**IMsTscAdvancedSettings::p UT \_ PluginDlls**](imstscadvancedsettings-plugindlls.md) del control ActiveX de protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="b051f-105">Invoking the [**IMsTscAdvancedSettings::put\_PluginDlls**](imstscadvancedsettings-plugindlls.md) method of the Remote Desktop Protocol (RDP) ActiveX control.</span></span> <span data-ttu-id="b051f-106">Varias entradas deben estar separadas por comas.</span><span class="sxs-lookup"><span data-stu-id="b051f-106">Multiple entries must be comma separated.</span></span>
-   <span data-ttu-id="b051f-107">Escribir la entrada del complemento en la siguiente ubicación del registro en el equipo en el que se inicia el proceso del cliente de Conexión a Escritorio remoto (RDC):</span><span class="sxs-lookup"><span data-stu-id="b051f-107">Writing the plug-in entry to the following location in the registry on the computer where the Remote Desktop Connection (RDC) client process is started:</span></span>

    <span data-ttu-id="b051f-108">**HKEY \_ Software de \_ usuario actual** \\  \\ **Microsoft** \\ **Terminal Server Client** \\ **predeterminados** \\ **AddIns** \\ ***nombre de complemento único***</span><span class="sxs-lookup"><span data-stu-id="b051f-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**AddIns**\\***unique plug-in name***</span></span>

    > [!Note]  
    > <span data-ttu-id="b051f-109">Debe crear la subclave del *nombre del complemento único* si no existe.</span><span class="sxs-lookup"><span data-stu-id="b051f-109">You must create the *unique plug-in name* subkey if it does not exist.</span></span> <span data-ttu-id="b051f-110">El nombre del *complemento único* nombre de la subclave es una cadena arbitraria que puede identificar el complemento.</span><span class="sxs-lookup"><span data-stu-id="b051f-110">The *unique plug-in name* subkey name is an arbitrary string that can identify the plug-in.</span></span> <span data-ttu-id="b051f-111">La cadena puede ser cualquier combinación de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b051f-111">The string can be any combination of characters.</span></span>

     

    <span data-ttu-id="b051f-112">En *nombre de complemento único*, debe agregar una entrada que identifique el complemento.</span><span class="sxs-lookup"><span data-stu-id="b051f-112">Under *unique plug-in name*, you must add an entry that identifies the plug-in.</span></span>

    <span data-ttu-id="b051f-113">Nombre de la entrada = **nombre**</span><span class="sxs-lookup"><span data-stu-id="b051f-113">Entry name = **Name**</span></span>

    <span data-ttu-id="b051f-114">Tipo de datos = **reg \_ SZ** o **reg \_ Expand \_**</span><span class="sxs-lookup"><span data-stu-id="b051f-114">Data type = **REG\_SZ** or **REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="b051f-115">En ambos casos, el valor de entrada debe ajustarse a uno de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="b051f-115">In both cases, the entry value must conform to one of the following formats:</span></span>

<dl> <dt>

<span data-ttu-id="b051f-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*: {*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="b051f-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*:{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="b051f-117">El complemento no se registra necesariamente en el registro de Windows como un objeto de modelo de objetos componentes (COM), pero el archivo DLL se implementa como un objeto COM en proceso.</span><span class="sxs-lookup"><span data-stu-id="b051f-117">The plug-in is not necessarily registered in the Windows registry as a Component Object Model (COM) object, but the DLL is implemented as an in-process COM object.</span></span> <span data-ttu-id="b051f-118">El cliente RDC cargará el archivo DLL especificado por *Plug-inDLLName* y recuperará el objeto com directamente mediante *CLSID*.</span><span class="sxs-lookup"><span data-stu-id="b051f-118">The RDC client will load the DLL specified by *Plug-inDLLName* and retrieve the COM object directly using *CLSID*.</span></span>

</dd> <dt>

<span data-ttu-id="b051f-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"</span><span class="sxs-lookup"><span data-stu-id="b051f-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"</span></span>
</dt> <dd>

<span data-ttu-id="b051f-120">El archivo DLL implementa la función [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) y lo exporta por su nombre.</span><span class="sxs-lookup"><span data-stu-id="b051f-120">The DLL implements the [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) function and exports it by name.</span></span> <span data-ttu-id="b051f-121">El cliente RDC usará la función **VirtualChannelGetInstance** para obtener punteros de interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos los complementos implementados por el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="b051f-121">The RDC client will use the **VirtualChannelGetInstance** function to obtain [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface pointers for all of the plug-ins implemented by the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="b051f-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="b051f-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="b051f-123">El cliente RDC creará una instancia del complemento como un objeto COM normal mediante [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con el *CLSID*.</span><span class="sxs-lookup"><span data-stu-id="b051f-123">The RDC client will instantiate the plug-in as a regular COM object using [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with the *CLSID*.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="b051f-124">*Plug-inDLLName* representa la ruta de acceso completa y el nombre de archivo del archivo. dll.</span><span class="sxs-lookup"><span data-stu-id="b051f-124">*Plug-inDLLName* represents the full path and file name of the .dll file.</span></span> <span data-ttu-id="b051f-125">Si el tipo de datos es **reg \_ Expand \_ SZ**, la ruta de acceso puede contener variables de entorno no expandidas que se expandan en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b051f-125">If the data type is **REG\_EXPAND\_SZ**, the path can contain unexpanded environment variables that are expanded at runtime.</span></span>

 

<span data-ttu-id="b051f-126">Cuando el cliente de Conexión a Escritorio remoto (RDC) finaliza la inicialización, realizará lo siguiente para cada complemento registrado:</span><span class="sxs-lookup"><span data-stu-id="b051f-126">When the Remote Desktop Connection (RDC) client finishes its initialization, it will perform the following for every registered plug-in:</span></span>

1.  <span data-ttu-id="b051f-127">Obtenga una instancia de la interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para cada complemento con uno de los métodos descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b051f-127">Obtain an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for each plug-in using one of the methods described above.</span></span>
2.  <span data-ttu-id="b051f-128">Llame al método [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) de cada interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) .</span><span class="sxs-lookup"><span data-stu-id="b051f-128">Call the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of each [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface.</span></span>
3.  <span data-ttu-id="b051f-129">Si el cliente se conecta varias veces al mismo servidor o a otro diferente, puede haber varias llamadas a los métodos [**conectados**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) y [**desconectados**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) .</span><span class="sxs-lookup"><span data-stu-id="b051f-129">If the client connects multiple times to the same or to a different server, there may be multiple calls to the [**Connected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) and [**Disconnected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) methods.</span></span>
4.  <span data-ttu-id="b051f-130">La última llamada que debe controlar el complemento ha [**finalizado**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span><span class="sxs-lookup"><span data-stu-id="b051f-130">The last call that the plug-in should handle is [**Terminated**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span></span> <span data-ttu-id="b051f-131">Es una señal de que el cliente Conexión a Escritorio remoto (RDC) está a punto de descargar el complemento.</span><span class="sxs-lookup"><span data-stu-id="b051f-131">It is a signal that the Remote Desktop Connection (RDC) client is about to unload the plug-in.</span></span>

 

 
---
title: Apertura de un dispositivo
description: Apertura de un dispositivo
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- Comando MCI_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077601"
---
# <a name="opening-a-device"></a><span data-ttu-id="7b573-104">Apertura de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="7b573-104">Opening a Device</span></span>

<span data-ttu-id="7b573-105">Antes de usar un dispositivo, debe inicializarlo con el comando [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="7b573-105">Before using a device, you must initialize it by using the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span> <span data-ttu-id="7b573-106">Este comando carga el controlador en la memoria (si aún no está cargado) y recupera el identificador de dispositivo que se usará para identificar el dispositivo en los comandos MCI posteriores.</span><span class="sxs-lookup"><span data-stu-id="7b573-106">This command loads the driver into memory (if it isn't already loaded) and retrieves the device identifier you will use to identify the device in subsequent MCI commands.</span></span> <span data-ttu-id="7b573-107">Debe comprobar el valor devuelto de la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) o [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) antes de usar un nuevo identificador de dispositivo para asegurarse de que el identificador es válido.</span><span class="sxs-lookup"><span data-stu-id="7b573-107">You should check the return value of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function before using a new device identifier to ensure that the identifier is valid.</span></span> <span data-ttu-id="7b573-108">(También puede recuperar un identificador de dispositivo mediante la función [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) ).</span><span class="sxs-lookup"><span data-stu-id="7b573-108">(You can also retrieve a device identifier by using the [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) function.)</span></span>

<span data-ttu-id="7b573-109">Al igual que todos los mensajes de comandos MCI, **MCI \_ Open** tiene una estructura asociada.</span><span class="sxs-lookup"><span data-stu-id="7b573-109">Like all MCI command messages, **MCI\_OPEN** has an associated structure.</span></span> <span data-ttu-id="7b573-110">Estas estructuras a veces se denominan *bloques de parámetros*.</span><span class="sxs-lookup"><span data-stu-id="7b573-110">These structures are sometimes called *parameter blocks*.</span></span> <span data-ttu-id="7b573-111">La estructura predeterminada de **MCI \_ Open** es [**MCI \_ Open \_ parms**](mci-open-parms.md).</span><span class="sxs-lookup"><span data-stu-id="7b573-111">The default structure for **MCI\_OPEN** is [**MCI\_OPEN\_PARMS**](mci-open-parms.md).</span></span> <span data-ttu-id="7b573-112">Algunos dispositivos (como la forma de *onda* y la *superposición*) tienen estructuras extendidas (como [**MCI \_ Wave \_ Open \_ parms**](mci-wave-open-parms.md) y [**MCI \_ OVLY \_ Open \_ parms**](mci-ovly-open-parms.md)) para dar cabida a parámetros opcionales adicionales.</span><span class="sxs-lookup"><span data-stu-id="7b573-112">Certain devices (such as *waveform* and *overlay*) have extended structures (such as [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) and [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md)) to accommodate additional optional parameters.</span></span> <span data-ttu-id="7b573-113">A menos que necesite usar estos parámetros adicionales, puede usar la estructura **MCI \_ Open \_ parms** con cualquier dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="7b573-113">Unless you need to use these additional parameters, you can use the **MCI\_OPEN\_PARMS** structure with any MCI device.</span></span>

<span data-ttu-id="7b573-114">El número de dispositivos que puede tener abiertos solo está limitado por la cantidad de memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="7b573-114">The number of devices you can have open is limited only by the amount of available memory.</span></span>

## <a name="using-an-alias"></a><span data-ttu-id="7b573-115">Usar un alias</span><span class="sxs-lookup"><span data-stu-id="7b573-115">Using an Alias</span></span>

<span data-ttu-id="7b573-116">Al abrir un dispositivo, puede usar la marca "alias" para especificar un identificador de dispositivo para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-116">When you open a device, you can use the "alias" flag to specify a device identifier for the device.</span></span> <span data-ttu-id="7b573-117">Esta marca permite asignar un identificador de dispositivo corto para dispositivos compuestos con nombres de archivo largos y permite abrir varias instancias del mismo archivo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-117">This flag lets you assign a short device identifier for compound devices with lengthy filenames, and it lets you open multiple instances of the same file or device.</span></span>

<span data-ttu-id="7b573-118">Por ejemplo, el siguiente comando asigna el identificador de dispositivo "birdcall" al nombre de archivo largo C: \\ NABIRDS \\ Sounds \\ MOCKMTNG. WAV</span><span class="sxs-lookup"><span data-stu-id="7b573-118">For example, the following command assigns the device identifier "birdcall" to the lengthy filename C:\\NABIRDS\\SOUNDS\\MOCKMTNG.WAV:</span></span>


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="7b573-119">En la interfaz de mensajes de comandos, especifique un alias mediante el miembro **lpstrAlias** de la estructura [**de \_ \_ parms abierto de MCI**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="7b573-119">In the command-message interface, you specify an alias by using the **lpstrAlias** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="specifying-a-device-type"></a><span data-ttu-id="7b573-120">Especificación de un tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="7b573-120">Specifying a Device Type</span></span>

<span data-ttu-id="7b573-121">Al abrir un dispositivo, puede usar la marca "tipo" para hacer referencia a un tipo de dispositivo, en lugar de a un controlador de dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="7b573-121">When you open a device, you can use the "type" flag to refer to a device type, rather than to a specific device driver.</span></span> <span data-ttu-id="7b573-122">En el siguiente ejemplo se abre el archivo de audio de forma de onda C: sonidos de \\ Windows \\ . WAV (mediante la marca "tipo" para especificar el tipo de dispositivo **WaveAudio** ) y asigna el alias "campanas":</span><span class="sxs-lookup"><span data-stu-id="7b573-122">The following example opens the waveform-audio file C:\\WINDOWS\\CHIMES.WAV (using the "type" flag to specify the **waveaudio** device type) and assigns the alias "chimes":</span></span>


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="7b573-123">En la interfaz de mensajes de comandos, el miembro **lpstrDeviceType** de la estructura de [**\_ \_ parms abierto de MCI**](mci-open-parms.md) proporciona la funcionalidad de la marca "tipo".</span><span class="sxs-lookup"><span data-stu-id="7b573-123">In the command-message interface, the functionality of the "type" flag is supplied by the **lpstrDeviceType** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="simple-and-compound-devices"></a><span data-ttu-id="7b573-124">Dispositivos simples y compuestos</span><span class="sxs-lookup"><span data-stu-id="7b573-124">Simple and Compound Devices</span></span>

<span data-ttu-id="7b573-125">MCI clasifica los controladores de dispositivos como *compuestos* o *simples*.</span><span class="sxs-lookup"><span data-stu-id="7b573-125">MCI classifies device drivers as *compound* or *simple*.</span></span> <span data-ttu-id="7b573-126">Los controladores de dispositivos compuestos requieren el nombre de un archivo de datos para la reproducción. los controladores para dispositivos sencillos no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="7b573-126">Drivers for compound devices require the name of a data file for playback; drivers for simple devices do not.</span></span>

<span data-ttu-id="7b573-127">Los dispositivos simples incluyen dispositivos **cdaudio** y **VideoDisc** .</span><span class="sxs-lookup"><span data-stu-id="7b573-127">Simple devices include **cdaudio** and **videodisc** devices.</span></span> <span data-ttu-id="7b573-128">Hay dos maneras de abrir dispositivos simples:</span><span class="sxs-lookup"><span data-stu-id="7b573-128">There are two ways to open simple devices:</span></span>

-   <span data-ttu-id="7b573-129">Especifique un puntero a una cadena terminada en null que contenga el nombre del dispositivo del registro o del archivo de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="7b573-129">Specify a pointer to a null-terminated string containing the device name from the registry or the SYSTEM.INI file.</span></span>

    <span data-ttu-id="7b573-130">Por ejemplo, puede abrir un dispositivo de **videodisco** con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="7b573-130">For example, you can open a **videodisc** device by using the following command:</span></span>


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="7b573-131">En este caso, "VideoDisc" es el nombre del dispositivo en el registro o en la \[ \] sección mci de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="7b573-131">In this case, "videodisc" is the device name from the registry or the \[mci\] section of SYSTEM.INI.</span></span>

-   <span data-ttu-id="7b573-132">Especifique el nombre real del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-132">Specify the actual name of the device driver.</span></span> <span data-ttu-id="7b573-133">La apertura de un dispositivo con el nombre de archivo del controlador de dispositivo, sin embargo, hace que la aplicación sea específica del dispositivo y puede impedir que la aplicación se ejecute si cambia la configuración del sistema.</span><span class="sxs-lookup"><span data-stu-id="7b573-133">Opening a device using the device-driver filename, however, makes the application device-specific and can prevent the application from running if the system configuration changes.</span></span> <span data-ttu-id="7b573-134">Si utiliza un nombre de archivo, no es necesario especificar la ruta de acceso completa o la extensión de nombre de archivo. MCI supone que los controladores se encuentran en un directorio del sistema y tienen el. Extensión de nombre de archivo DRV.</span><span class="sxs-lookup"><span data-stu-id="7b573-134">If you use a filename, you do not need to specify the complete path or the filename extension; MCI assumes drivers are located in a system directory and have the .DRV filename extension.</span></span>

<span data-ttu-id="7b573-135">Los dispositivos compuestos incluyen **WaveAudio** y los dispositivos **Sequencer** .</span><span class="sxs-lookup"><span data-stu-id="7b573-135">Compound devices include **waveaudio** and **sequencer** devices.</span></span> <span data-ttu-id="7b573-136">Los datos de un dispositivo compuesto se denominan a veces *elemento de dispositivo*.</span><span class="sxs-lookup"><span data-stu-id="7b573-136">The data for a compound device is sometimes called a *device element*.</span></span> <span data-ttu-id="7b573-137">Sin embargo, este documento normalmente hace referencia a estos datos como un archivo, aunque en algunos casos es posible que los datos no se almacenen como un archivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-137">This document, however, generally refers to this data as a file, even though in some cases the data might not be stored as a file.</span></span>

<span data-ttu-id="7b573-138">Hay tres maneras de abrir un dispositivo compuesto:</span><span class="sxs-lookup"><span data-stu-id="7b573-138">There are three ways to open a compound device:</span></span>

-   <span data-ttu-id="7b573-139">Especifique solo el nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-139">Specify only the device name.</span></span> <span data-ttu-id="7b573-140">Esto le permite abrir un dispositivo compuesto sin asociar un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-140">This lets you open a compound device without associating a filename.</span></span> <span data-ttu-id="7b573-141">La mayoría de los dispositivos compuestos solo procesan los comandos [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) y [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)) cuando se abren de esta manera.</span><span class="sxs-lookup"><span data-stu-id="7b573-141">Most compound devices process only the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) commands when they are opened this way.</span></span>
-   <span data-ttu-id="7b573-142">Especifique solo el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-142">Specify only the filename.</span></span> <span data-ttu-id="7b573-143">El nombre del dispositivo se determina a partir de las asociaciones del registro.</span><span class="sxs-lookup"><span data-stu-id="7b573-143">The device name is determined from the associations in the registry.</span></span>
-   <span data-ttu-id="7b573-144">Especifique el nombre de archivo y el nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-144">Specify the filename and the device name.</span></span> <span data-ttu-id="7b573-145">MCI omite las entradas en el registro y abre el nombre del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7b573-145">MCI ignores the entries in the registry and opens the specified device name.</span></span>

<span data-ttu-id="7b573-146">Para asociar un archivo de datos a un dispositivo determinado, puede especificar el nombre de archivo y el nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-146">To associate a data file with a particular device, you can specify the filename and device name.</span></span> <span data-ttu-id="7b573-147">Por ejemplo, el siguiente comando abre el dispositivo **WaveAudio** con el nombre de archivo de la voz. SND</span><span class="sxs-lookup"><span data-stu-id="7b573-147">For example, the following command opens the **waveaudio** device with the filename MYVOICE.SND:</span></span>


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="7b573-148">En la interfaz de cadena de comandos, también puede abreviar la especificación de nombre de dispositivo mediante el formato de signo de exclamación alternativo, como se documenta con el comando [**abrir**](open.md) .</span><span class="sxs-lookup"><span data-stu-id="7b573-148">In the command-string interface, you can also abbreviate the device name specification by using the alternative exclamation-point format, as documented with the [**open**](open.md) command.</span></span>

## <a name="opening-a-device-using-the-filename-extension"></a><span data-ttu-id="7b573-149">Abrir un dispositivo con la extensión de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="7b573-149">Opening a Device Using the Filename Extension</span></span>

<span data-ttu-id="7b573-150">Si el comando [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)) especifica solo el nombre de archivo, MCI usa la extensión de nombre de archivo para seleccionar el dispositivo adecuado en la lista del registro o en la \[ \] sección de extensiones MCI del archivo de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="7b573-150">If the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command specifies only the filename, MCI uses the filename extension to select the appropriate device from the list in the registry or the \[mci extensions\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="7b573-151">Las entradas de la \[ sección de extensiones MCI \] usan el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="7b573-151">The entries in the \[mci extensions\] section use the following form:</span></span>

<span data-ttu-id="7b573-152">*\_*  =  *\_ nombre del dispositivo* de extensión de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="7b573-152">*filename\_extension* = *device\_name*</span></span>

<span data-ttu-id="7b573-153">MCI usa implícitamente *el \_ nombre del dispositivo* si se encuentra la extensión y si no se ha especificado un nombre de dispositivo en el comando **abrir** .</span><span class="sxs-lookup"><span data-stu-id="7b573-153">MCI implicitly uses *device\_name* if the extension is found and if a device name has not been specified in the **open** command.</span></span>

<span data-ttu-id="7b573-154">En el ejemplo siguiente se muestra una \[ sección de extensiones MCI típica \] :</span><span class="sxs-lookup"><span data-stu-id="7b573-154">The following example shows a typical \[mci extensions\] section:</span></span>


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



<span data-ttu-id="7b573-155">Con estas definiciones, MCI abre el dispositivo **WaveAudio** si se emite el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="7b573-155">Using these definitions, MCI opens the **waveaudio** device if the following command is issued:</span></span>


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a><span data-ttu-id="7b573-156">Nuevos archivos de datos</span><span class="sxs-lookup"><span data-stu-id="7b573-156">New Data Files</span></span>

<span data-ttu-id="7b573-157">Para crear un nuevo archivo de datos, solo tiene que especificar un nombre de archivo en blanco.</span><span class="sxs-lookup"><span data-stu-id="7b573-157">To create a new data file, simply specify a blank filename.</span></span> <span data-ttu-id="7b573-158">MCI no guarda un archivo nuevo hasta que lo guarde con el comando [**Guardar**](save.md) ([**MCI \_ Save**](mci-save.md)).</span><span class="sxs-lookup"><span data-stu-id="7b573-158">MCI does not save a new file until you save it by using the [**save**](save.md) ([**MCI\_SAVE**](mci-save.md)) command.</span></span> <span data-ttu-id="7b573-159">Al crear un nuevo archivo, debe incluir un alias de dispositivo con el comando [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="7b573-159">When creating a new file, you must include a device alias with the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="7b573-160">En el ejemplo siguiente se abre un nuevo archivo **WaveAudio** , se inicia y se detiene la grabación y, a continuación, se guarda y se cierra el archivo:</span><span class="sxs-lookup"><span data-stu-id="7b573-160">The following example opens a new **waveaudio** file, starts and stops recording, then saves and closes the file:</span></span>


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a><span data-ttu-id="7b573-161">Dispositivos que se van a compartir</span><span class="sxs-lookup"><span data-stu-id="7b573-161">Sharable Devices</span></span>

<span data-ttu-id="7b573-162">La marca "compartible" (MCI \_ Open \_ Shareable) del comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) permite que varias aplicaciones tengan acceso simultáneamente al mismo dispositivo (o archivo) e instancia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-162">The "sharable" (MCI\_OPEN\_SHAREABLE) flag of the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command lets multiple applications access the same device (or file) and device instance simultaneously.</span></span> <span data-ttu-id="7b573-163">Si la aplicación abre un dispositivo o un archivo como compartido, otras aplicaciones también pueden tener acceso al mismo abriéndolo como compartible.</span><span class="sxs-lookup"><span data-stu-id="7b573-163">If your application opens a device or file as sharable, other applications can also access it by opening it as sharable.</span></span> <span data-ttu-id="7b573-164">El dispositivo o archivo compartido proporciona a cada aplicación la capacidad de cambiar los parámetros que rigen su estado operativo.</span><span class="sxs-lookup"><span data-stu-id="7b573-164">The shared device or file gives each application the ability to change the parameters governing its operating state.</span></span> <span data-ttu-id="7b573-165">Cada vez que un dispositivo o un archivo se abre como compartido, MCI devuelve un identificador de dispositivo único, aunque los identificadores hagan referencia a la misma instancia.</span><span class="sxs-lookup"><span data-stu-id="7b573-165">Each time a device or file is opened as sharable, MCI returns a unique device identifier, even though the identifiers refer to the same instance.</span></span>

<span data-ttu-id="7b573-166">Si la aplicación abre un dispositivo o un archivo sin especificar que se pueda compartir, ninguna otra aplicación podrá tener acceso a él hasta que la aplicación lo cierre.</span><span class="sxs-lookup"><span data-stu-id="7b573-166">If your application opens a device or file without specifying that it is sharable, no other application can access it until your application closes it.</span></span> <span data-ttu-id="7b573-167">Además, si un dispositivo solo admite una instancia abierta, el comando **Open** producirá un error si se especifica la marca compartible.</span><span class="sxs-lookup"><span data-stu-id="7b573-167">Also, if a device supports only one open instance, the **open** command will fail if you specify the sharable flag.</span></span>

<span data-ttu-id="7b573-168">Si la aplicación abre un dispositivo y especifica que se pueda compartir, la aplicación no debe hacer ninguna suposición sobre el estado de este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-168">If your application opens a device and specifies that it is sharable, your application should not make any assumptions about the state of this device.</span></span> <span data-ttu-id="7b573-169">Es posible que la aplicación necesite compensar los cambios realizados por otras aplicaciones que acceden al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-169">Your application might need to compensate for changes made by other applications accessing the device.</span></span>

<span data-ttu-id="7b573-170">La mayoría de los archivos compuestos no se pueden compartir. sin embargo, puede abrir varios archivos, o puede abrir un solo archivo varias veces.</span><span class="sxs-lookup"><span data-stu-id="7b573-170">Most compound files are not sharable; however, you can open multiple files, or you can open a single file multiple times.</span></span> <span data-ttu-id="7b573-171">Si abre un solo archivo varias veces, MCI crea una instancia independiente para cada una de ellas con un estado operativo único.</span><span class="sxs-lookup"><span data-stu-id="7b573-171">If you open a single file multiple times, MCI creates an independent instance for each, with each instance having a unique operating status.</span></span>

<span data-ttu-id="7b573-172">Si abre varias instancias de un archivo, debe asignar un identificador de dispositivo único a cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="7b573-172">If you open multiple instances of a file, you must assign a unique device identifier to each.</span></span> <span data-ttu-id="7b573-173">Puede usar un alias, como se describe en la sección siguiente, para asignar un nombre único a cada archivo.</span><span class="sxs-lookup"><span data-stu-id="7b573-173">You can use an alias, as described in the following section, to assign a unique name for each file.</span></span>

 

 
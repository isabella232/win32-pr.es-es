---
title: TaskService. Connect (método)
description: Para el scripting, se conecta a un equipo remoto y asocia todas las llamadas subsiguientes en esta interfaz a una sesión remota.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Método Connect Programador de tareas
- Método Connect Programador de tareas, objeto TaskService
- Programador de tareas de objeto TaskService, método Connect
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996155"
---
# <a name="taskserviceconnect-method"></a><span data-ttu-id="01596-106">TaskService. Connect (método)</span><span class="sxs-lookup"><span data-stu-id="01596-106">TaskService.Connect method</span></span>

<span data-ttu-id="01596-107">Para el scripting, se conecta a un equipo remoto y asocia todas las llamadas subsiguientes en esta interfaz a una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="01596-107">For scripting, connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span> <span data-ttu-id="01596-108">Si el parámetro serverName está vacío, este método se ejecutará en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="01596-108">If the serverName parameter is empty, then this method will execute on the local computer.</span></span> <span data-ttu-id="01596-109">Si no se especifica userId, se usa el token actual.</span><span class="sxs-lookup"><span data-stu-id="01596-109">If the userId is not specified, then the current token is used.</span></span>

## <a name="syntax"></a><span data-ttu-id="01596-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01596-110">Syntax</span></span>


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="01596-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01596-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01596-112">*nombreDeServidor* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="01596-112">*serverName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01596-113">Nombre del equipo al que desea conectarse.</span><span class="sxs-lookup"><span data-stu-id="01596-113">The name of the computer that you want to connect to.</span></span> <span data-ttu-id="01596-114">Si el parámetro serverName está vacío, este método se ejecutará en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="01596-114">If the serverName parameter is empty, then this method will execute on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="01596-115">*usuario* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="01596-115">*user* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01596-116">El nombre de usuario que se usa durante la conexión al equipo.</span><span class="sxs-lookup"><span data-stu-id="01596-116">The user name that is used during the connection to the computer.</span></span> <span data-ttu-id="01596-117">Si no se especifica el usuario, se usa el token actual.</span><span class="sxs-lookup"><span data-stu-id="01596-117">If the user is not specified, then the current token is used.</span></span>

</dd> <dt>

<span data-ttu-id="01596-118">*dominio* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="01596-118">*domain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01596-119">Dominio del usuario especificado en el parámetro de *usuario* .</span><span class="sxs-lookup"><span data-stu-id="01596-119">The domain of the user specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="01596-120">*contraseña* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="01596-120">*password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01596-121">La contraseña que se utiliza para conectarse al equipo.</span><span class="sxs-lookup"><span data-stu-id="01596-121">The password that is used to connect to the computer.</span></span> <span data-ttu-id="01596-122">Si no se especifican el nombre de usuario y la contraseña, se usa el token actual.</span><span class="sxs-lookup"><span data-stu-id="01596-122">If the user name and password are not specified, then the current token is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01596-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01596-123">Return value</span></span>

<span data-ttu-id="01596-124">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="01596-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01596-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01596-125">Remarks</span></span>

<span data-ttu-id="01596-126">Se debe llamar al método **TaskService. Connect** antes de llamar a cualquiera de los otros métodos [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="01596-126">The **TaskService.Connect** method should be called before calling any of the other [**TaskService**](taskservice.md) methods.</span></span>

<span data-ttu-id="01596-127">Si se produce un error en el método Connect, puede recopilar el identificador de error para encontrar el significado del error.</span><span class="sxs-lookup"><span data-stu-id="01596-127">If the Connect method fails, you can collect the error identifier to find the meaning of the error.</span></span> <span data-ttu-id="01596-128">En la tabla siguiente se enumeran los identificadores de error y sus descripciones.</span><span class="sxs-lookup"><span data-stu-id="01596-128">The following table lists the error identifiers and their descriptions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01596-129">Identificador de error</span><span class="sxs-lookup"><span data-stu-id="01596-129">Error Identifier</span></span></th>
<th><span data-ttu-id="01596-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="01596-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01596-131">0x80070005</span><span class="sxs-lookup"><span data-stu-id="01596-131">0x80070005</span></span></td>
<td><span data-ttu-id="01596-132">Se denegó el acceso para conectarse al servicio de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="01596-132">Access is denied to connect to the Task Scheduler service.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01596-133">0x80041315</span><span class="sxs-lookup"><span data-stu-id="01596-133">0x80041315</span></span></td>
<td><span data-ttu-id="01596-134">El servicio Programador de tareas no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="01596-134">The Task Scheduler service is not running.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01596-135">0x8007000e</span><span class="sxs-lookup"><span data-stu-id="01596-135">0x8007000e</span></span></td>
<td><span data-ttu-id="01596-136">La aplicación no tiene suficiente memoria para completar la operación o el <em>usuario</em>, la <em>contraseña</em>o el <em>dominio</em> tiene al menos un valor NULL y un valor distinto de NULL.</span><span class="sxs-lookup"><span data-stu-id="01596-136">The application does not have enough memory to complete the operation or the <em>user</em>, <em>password</em>, or <em>domain</em> has at least one null and one non-null value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01596-137">53</span><span class="sxs-lookup"><span data-stu-id="01596-137">53</span></span></td>
<td><span data-ttu-id="01596-138">Este error se devuelve en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="01596-138">This error is returned in the following situations:</span></span>
<ul>
<li><span data-ttu-id="01596-139">El nombre de equipo especificado en el parámetro <em>ServerName</em> no existe.</span><span class="sxs-lookup"><span data-stu-id="01596-139">The computer name specified in the <em>serverName</em> parameter does not exist.</span></span></li>
<li><span data-ttu-id="01596-140">Cuando intenta conectarse a un equipo con Windows Server 2003 o Windows XP, y el equipo remoto no tiene la excepción de Firewall compartir archivos e impresoras habilitada o el servicio de registro remoto no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="01596-140">When you are trying to connect to a Windows Server 2003 or Windows XP computer, and the remote computer does not have the File and Printer Sharing firewall exception enabled or the Remote Registry service is not running.</span></span></li>
<li><span data-ttu-id="01596-141">Cuando intenta conectarse a un equipo con Windows Vista, y el equipo remoto no tiene habilitada la excepción del firewall administración remota de tareas programadas y la excepción de Firewall compartir archivos e impresoras está habilitada, o el servicio registro remoto no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="01596-141">When you are trying to connect to a Windows Vista computer, and the remote computer does not have the Remote Scheduled Tasks Management firewall exception enabled and the File and Printer Sharing firewall exception enabled, or the Remote Registry service is not running.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01596-142">50</span><span class="sxs-lookup"><span data-stu-id="01596-142">50</span></span></td>
<td><span data-ttu-id="01596-143">Los parámetros <em>User</em>, <em>password</em>o <em>Domain</em> no se pueden especificar al conectarse a un equipo remoto con Windows XP o Windows Server 2003 desde un equipo con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="01596-143">The <em>user</em>, <em>password</em>, or <em>domain</em> parameters cannot be specified when connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="01596-144">Si va a conectarse a un equipo remoto de Windows Vista desde Windows Vista, debe permitir la excepción del firewall administración remota de tareas programadas en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="01596-144">If you are to connecting to a remote Windows Vista computer from a Windows Vista, you need to allow the Remote Scheduled Tasks Management firewall exception on the remote computer.</span></span> <span data-ttu-id="01596-145">Para permitir esta excepción, haga clic en Inicio, Panel de control, Seguridad, Dejar pasar a un programa a través de Firewall de Windows y, a continuación, active la casilla Administración remota de tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="01596-145">To allow this exception click Start, Control Panel, Security, Allow a program through Windows Firewall, and then select the Remote Scheduled Tasks Management check box.</span></span> <span data-ttu-id="01596-146">A continuación, haga clic en el botón Aceptar en el cuadro de diálogo Configuración de Firewall de Windows.</span><span class="sxs-lookup"><span data-stu-id="01596-146">Then click the Ok button in the Windows Firewall Settings dialog box.</span></span>

<span data-ttu-id="01596-147">Si va a conectarse a un equipo remoto equipado con Windows XP o Windows Server 2003 desde un equipo equipado con Windows Vista, necesita permitir la excepción de firewall Compartir archivos e impresoras en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="01596-147">If you are connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer, you need to allow the File and Printer Sharing firewall exception on the remote computer.</span></span> <span data-ttu-id="01596-148">Para permitir esta excepción, haga clic en Inicio, Panel de control, haga doble clic en Firewall de Windows, seleccione la ficha Excepciones y, a continuación, seleccione la excepción de firewall Compartir archivos e impresoras.</span><span class="sxs-lookup"><span data-stu-id="01596-148">To allow this exception click Start, Control Panel, double-click Windows Firewall, select the Exceptions tab, and then select the File and Printer Sharing firewall exception.</span></span> <span data-ttu-id="01596-149">A continuación, haga clic en el botón Aceptar del cuadro de diálogo Firewall de Windows.</span><span class="sxs-lookup"><span data-stu-id="01596-149">Then click the OK button in the Windows Firewall dialog box.</span></span> <span data-ttu-id="01596-150">El servicio de registro remoto también debe estar en ejecución en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="01596-150">The Remote Registry service must also be running on the remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="01596-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01596-151">Requirements</span></span>



| <span data-ttu-id="01596-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="01596-152">Requirement</span></span> | <span data-ttu-id="01596-153">Value</span><span class="sxs-lookup"><span data-stu-id="01596-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01596-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01596-154">Minimum supported client</span></span><br/> | <span data-ttu-id="01596-155">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="01596-155">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="01596-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01596-156">Minimum supported server</span></span><br/> | <span data-ttu-id="01596-157">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="01596-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="01596-158">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="01596-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="01596-159"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01596-159"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01596-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01596-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01596-161"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01596-161"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 






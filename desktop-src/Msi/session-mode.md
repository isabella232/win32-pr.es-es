---
description: Esta es la propiedad Mode del objeto Session. Esta propiedad es un valor que representa la marca de modo designado para la sesión de instalación actual. La mayoría de las marcas de modo son de solo lectura externamente, pero también se pueden establecer algunas marcas especificadas.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Propiedad Session. Mode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: f081859db789601f2c41bf95d65c377fba8d51f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681129"
---
# <a name="sessionmode-property"></a><span data-ttu-id="02d5d-105">Propiedad Session. Mode</span><span class="sxs-lookup"><span data-stu-id="02d5d-105">Session.Mode property</span></span>

<span data-ttu-id="02d5d-106">Esta es la propiedad **mode** del objeto [**Session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="02d5d-106">This is the **Mode** property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="02d5d-107">Esta propiedad es un valor que representa la marca de modo designado para la sesión de instalación actual.</span><span class="sxs-lookup"><span data-stu-id="02d5d-107">This property is a value representing the designated mode flag for the current install session.</span></span> <span data-ttu-id="02d5d-108">La mayoría de las marcas de modo son de solo lectura externamente, pero también se pueden establecer algunas marcas especificadas.</span><span class="sxs-lookup"><span data-stu-id="02d5d-108">Most of the mode flags are read-only externally, but a few specified flags may be set as well.</span></span>

<span data-ttu-id="02d5d-109">La función [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) devuelve un valor booleano true o false, que indica si la propiedad específica que se pasa a la función está establecida actualmente (true) o no (false).</span><span class="sxs-lookup"><span data-stu-id="02d5d-109">The [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function returns a Boolean TRUE or FALSE, indicating whether the specific property passed into the function is currently set (TRUE) or not set (FALSE).</span></span>

<span data-ttu-id="02d5d-110">Tenga en cuenta que no todos los valores de los modos de ejecución de *Flag* están disponibles al llamar a la propiedad **mode** desde una acción personalizada diferida.</span><span class="sxs-lookup"><span data-stu-id="02d5d-110">Note that not all the run mode values of *flag* are available when calling the **Mode** property from a deferred custom action.</span></span> <span data-ttu-id="02d5d-111">Para obtener más información, vea [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="02d5d-111">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="02d5d-112">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="02d5d-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d5d-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02d5d-113">Syntax</span></span>


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a><span data-ttu-id="02d5d-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="02d5d-114">Property value</span></span>

<span data-ttu-id="02d5d-115">Valor entero necesario para la marca.</span><span class="sxs-lookup"><span data-stu-id="02d5d-115">Required integer value for the flag.</span></span> <span data-ttu-id="02d5d-116">Debe ser una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="02d5d-116">Must be one of the following:</span></span>



| <span data-ttu-id="02d5d-117">Nombre del marcador</span><span class="sxs-lookup"><span data-stu-id="02d5d-117">Flag name</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="02d5d-118">Significado</span><span class="sxs-lookup"><span data-stu-id="02d5d-118">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <span data-ttu-id="02d5d-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="02d5d-120">Instalación del modo administrativo; de lo contrario, instale el producto.</span><span class="sxs-lookup"><span data-stu-id="02d5d-120">Administrative mode install, else product install.</span></span><br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <span data-ttu-id="02d5d-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="02d5d-122">Modo de anuncio de instalación.</span><span class="sxs-lookup"><span data-stu-id="02d5d-122">Advertise mode of install.</span></span><br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <span data-ttu-id="02d5d-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="02d5d-124">Base de datos de modo de mantenimiento cargada.</span><span class="sxs-lookup"><span data-stu-id="02d5d-124">Maintenance mode database loaded.</span></span><br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <span data-ttu-id="02d5d-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="02d5d-126">La reversión está habilitada.</span><span class="sxs-lookup"><span data-stu-id="02d5d-126">Rollback is enabled.</span></span><br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <span data-ttu-id="02d5d-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="02d5d-128">El archivo de registro está activo.</span><span class="sxs-lookup"><span data-stu-id="02d5d-128">Log file is active.</span></span><br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <span data-ttu-id="02d5d-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span></span> </dl>                          | <span data-ttu-id="02d5d-130">Ejecución o puesta en cola de operaciones.</span><span class="sxs-lookup"><span data-stu-id="02d5d-130">Executing or spooling operations.</span></span><br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <span data-ttu-id="02d5d-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span></span> </dl>                      | <span data-ttu-id="02d5d-132">Es necesario reiniciar (configurable).</span><span class="sxs-lookup"><span data-stu-id="02d5d-132">Reboot is needed (settable).</span></span><br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <span data-ttu-id="02d5d-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span></span> </dl>                              | <span data-ttu-id="02d5d-134">Es necesario reiniciar para continuar con la instalación (configurable).</span><span class="sxs-lookup"><span data-stu-id="02d5d-134">Reboot is needed to continue installation (settable).</span></span><br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <span data-ttu-id="02d5d-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span></span> </dl>                                      | <span data-ttu-id="02d5d-136">Instalación de archivos desde archivadores y archivos mediante la tabla de medios.</span><span class="sxs-lookup"><span data-stu-id="02d5d-136">Installing files from cabinets and files using Media table.</span></span><br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <span data-ttu-id="02d5d-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="02d5d-138">Los archivos de código fuente solo utilizan nombres de archivo cortos.</span><span class="sxs-lookup"><span data-stu-id="02d5d-138">Source files use only short file names.</span></span><br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <span data-ttu-id="02d5d-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="02d5d-140">Los archivos de destino solo utilizan nombres de archivo cortos.</span><span class="sxs-lookup"><span data-stu-id="02d5d-140">Target files are to use only short file names.</span></span><br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <span data-ttu-id="02d5d-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span></span> </dl>                             | <span data-ttu-id="02d5d-142">El sistema operativo es Windows 98/95.</span><span class="sxs-lookup"><span data-stu-id="02d5d-142">Operating system is Windows 98/95.</span></span><br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <span data-ttu-id="02d5d-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span></span> </dl>                         | <span data-ttu-id="02d5d-144">El sistema operativo admite la publicidad de productos.</span><span class="sxs-lookup"><span data-stu-id="02d5d-144">Operating system supports advertising of products.</span></span><br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <span data-ttu-id="02d5d-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span></span> </dl>                             | <span data-ttu-id="02d5d-146">[Acción personalizada](custom-actions.md) diferida llamada desde la ejecución del script de instalación.</span><span class="sxs-lookup"><span data-stu-id="02d5d-146">Deferred [custom action](custom-actions.md) called from install script execution.</span></span><br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <span data-ttu-id="02d5d-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="02d5d-148">[Acción personalizada](custom-actions.md) diferida a la que se llama desde el script de ejecución de reversión.</span><span class="sxs-lookup"><span data-stu-id="02d5d-148">Deferred [custom action](custom-actions.md) called from rollback execution script.</span></span><br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <span data-ttu-id="02d5d-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="02d5d-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span></span> </dl>                                         | <span data-ttu-id="02d5d-150">[Acción personalizada](custom-actions.md) diferida a la que se llama desde el script de ejecución de confirmación.</span><span class="sxs-lookup"><span data-stu-id="02d5d-150">Deferred [custom action](custom-actions.md) called from commit execution script.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="02d5d-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02d5d-151">Requirements</span></span>



| <span data-ttu-id="02d5d-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="02d5d-152">Requirement</span></span> | <span data-ttu-id="02d5d-153">Value</span><span class="sxs-lookup"><span data-stu-id="02d5d-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02d5d-154">Versión</span><span class="sxs-lookup"><span data-stu-id="02d5d-154">Version</span></span><br/> | <span data-ttu-id="02d5d-155">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02d5d-155">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="02d5d-156">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="02d5d-156">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="02d5d-157">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="02d5d-157">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



 

 





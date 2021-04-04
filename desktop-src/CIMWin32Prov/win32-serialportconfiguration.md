---
description: La \_ clase WMI SerialPortConfiguration de Win32 representa la configuración para la transmisión de datos en un puerto serie basado en Windows. Esto incluye configuraciones para establecer una conexión y comprobación de errores.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Win32_SerialPortConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998125"
---
# <a name="win32_serialportconfiguration-class"></a><span data-ttu-id="aeaac-104">\_Clase Win32 SerialPortConfiguration</span><span class="sxs-lookup"><span data-stu-id="aeaac-104">Win32\_SerialPortConfiguration class</span></span>

<span data-ttu-id="aeaac-105">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPortConfiguration de Win32** representa la configuración para la transmisión de datos en un puerto serie basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="aeaac-105">The **Win32\_SerialPortConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings for data transmission on a Windows-based serial port.</span></span> <span data-ttu-id="aeaac-106">Esto incluye configuraciones para establecer una conexión y comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="aeaac-106">This includes configurations for establishing a connection and error checking.</span></span>

<span data-ttu-id="aeaac-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="aeaac-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="aeaac-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="aeaac-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeaac-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aeaac-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a><span data-ttu-id="aeaac-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="aeaac-110">Members</span></span>

<span data-ttu-id="aeaac-111">La **clase \_ SerialPortConfiguration de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aeaac-111">The **Win32\_SerialPortConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="aeaac-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aeaac-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aeaac-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aeaac-113">Properties</span></span>

<span data-ttu-id="aeaac-114">La **clase \_ SerialPortConfiguration de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="aeaac-114">The **Win32\_SerialPortConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aeaac-115">**AbortReadWriteOnError**</span><span class="sxs-lookup"><span data-stu-id="aeaac-115">**AbortReadWriteOnError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aeaac-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-118">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError")</span><span class="sxs-lookup"><span data-stu-id="aeaac-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fAbortOnError")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-119">Si **es true**, las operaciones de lectura y escritura se terminan si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="aeaac-119">If **TRUE**, read and write operations are terminated if an error occurs.</span></span> <span data-ttu-id="aeaac-120">Si **es true**, el controlador finaliza todas las operaciones de lectura y escritura con un estado de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="aeaac-120">If **TRUE**, the driver terminates all read and write operations with an error status if an error occurs.</span></span> <span data-ttu-id="aeaac-121">El controlador no aceptará ninguna otra operación de comunicaciones hasta que la aplicación confirme el error.</span><span class="sxs-lookup"><span data-stu-id="aeaac-121">The driver will not accept any further communications operations until the application acknowledges the error.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-122">**BaudRate**</span><span class="sxs-lookup"><span data-stu-id="aeaac-122">**BaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-123">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeaac-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-125">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Baudrate")</span><span class="sxs-lookup"><span data-stu-id="aeaac-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|BaudRate")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-126">Velocidad en baudios (bits por segundo) a la que opera el dispositivo de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="aeaac-126">Baud (bits per second) rate at which the communications device operates.</span></span>

<span data-ttu-id="aeaac-127">Ejemplo: 9600</span><span class="sxs-lookup"><span data-stu-id="aeaac-127">Example: 9600</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-128">**BinaryModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="aeaac-128">**BinaryModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aeaac-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-131">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")</span><span class="sxs-lookup"><span data-stu-id="aeaac-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-132">Si **es true**, las transferencias de datos en modo binario están habilitadas para el puerto serie.</span><span class="sxs-lookup"><span data-stu-id="aeaac-132">If **TRUE**, binary-mode data transfers are enabled for the serial port.</span></span> <span data-ttu-id="aeaac-133">Los sistemas de equipos que ejecutan Windows solo permiten las transferencias binarias a través de puertos serie, por lo que este valor siempre es **true**.</span><span class="sxs-lookup"><span data-stu-id="aeaac-133">Computer systems running Windows only allow binary transfers through serial ports, so this value is always **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-134">**BitsPerByte**</span><span class="sxs-lookup"><span data-stu-id="aeaac-134">**BitsPerByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeaac-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-137">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ByteSize")</span><span class="sxs-lookup"><span data-stu-id="aeaac-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ByteSize")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-138">Número de bits transmitidos y recibidos por cada byte de datos para el puerto serie de Windows.</span><span class="sxs-lookup"><span data-stu-id="aeaac-138">Number of bits transmitted and received for each byte of data for the Windows serial port.</span></span> <span data-ttu-id="aeaac-139">El número puede variar con los bits de control y corrección de errores, como los bits de paridad.</span><span class="sxs-lookup"><span data-stu-id="aeaac-139">The number may vary with control and error correction bits, such as parity bits.</span></span>

<span data-ttu-id="aeaac-140">Ejemplo: 8</span><span class="sxs-lookup"><span data-stu-id="aeaac-140">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-141">**Caption**</span><span class="sxs-lookup"><span data-stu-id="aeaac-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeaac-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-144">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="aeaac-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-145">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="aeaac-145">Short textual description of the current object.</span></span>

<span data-ttu-id="aeaac-146">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="aeaac-146">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-147">**ContinueXMitOnXOff**</span><span class="sxs-lookup"><span data-stu-id="aeaac-147">**ContinueXMitOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-148">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aeaac-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-150">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff")</span><span class="sxs-lookup"><span data-stu-id="aeaac-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fTXContinueOnXoff")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-151">Si **es true**, las transmisiones de datos continúan cuando el búfer de entrada se encuentra en **XOffXmitThreshold** bytes de estar llenos y el controlador ha transmitido el valor **XOffChararcter** para dejar de recibir bytes.</span><span class="sxs-lookup"><span data-stu-id="aeaac-151">If **TRUE**, data transmissions continue when the input buffer has come within **XOffXMitThreshold** bytes of being full and the driver has transmitted the **XOffChararcter** value to stop receiving bytes.</span></span> <span data-ttu-id="aeaac-152">Si es **false**, la transmisión no continúa hasta que el búfer de entrada está dentro de **XOnXMitThreshold** bytes de estar vacío y el controlador ha transmitido el valor **XOnCharacter** para reanudar la recepción.</span><span class="sxs-lookup"><span data-stu-id="aeaac-152">If **FALSE**, transmission does not continue until the input buffer is within **XOnXMitThreshold** bytes of being empty and the driver has transmitted the **XOnCharacter** value to resume reception.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-153">**CTSOutflowControl**</span><span class="sxs-lookup"><span data-stu-id="aeaac-153">**CTSOutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-154">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aeaac-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-156">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow")</span><span class="sxs-lookup"><span data-stu-id="aeaac-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxCtsFlow")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-157">Si es **true**, se comprueba la señal de borrar para enviar (CTS) antes de transmitir datos.</span><span class="sxs-lookup"><span data-stu-id="aeaac-157">If **TRUE**, the clear to send (CTS) signal is checked before transmitting data.</span></span> <span data-ttu-id="aeaac-158">CTS indica que ambos dispositivos de la conexión serie están listos para transferir datos.</span><span class="sxs-lookup"><span data-stu-id="aeaac-158">CTS signals that both devices on the serial connection are ready to transfer data.</span></span> <span data-ttu-id="aeaac-159">La transmisión de datos se suspende hasta que se proporciona la señal CTS.</span><span class="sxs-lookup"><span data-stu-id="aeaac-159">Data transmission is suspended until the CTS signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-160">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aeaac-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeaac-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-163">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="aeaac-163">Textual description of the current object.</span></span>

<span data-ttu-id="aeaac-164">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="aeaac-164">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-165">**DiscardNULLBytes**</span><span class="sxs-lookup"><span data-stu-id="aeaac-165">**DiscardNULLBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-166">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aeaac-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-168">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull")</span><span class="sxs-lookup"><span data-stu-id="aeaac-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fNull")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-169">Si **es true**, los bytes **nulos** (caracteres) se descartan cuando se reciben.</span><span class="sxs-lookup"><span data-stu-id="aeaac-169">If **TRUE**, **NULL** bytes (characters) are discarded when they are received.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-170">**DSROutflowControl**</span><span class="sxs-lookup"><span data-stu-id="aeaac-170">**DSROutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-171">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aeaac-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-173">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow")</span><span class="sxs-lookup"><span data-stu-id="aeaac-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxDsrFlow")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-174">Si es **true**, el control de flujo de salida de datos está habilitado cuando hay una condición de conjunto de datos preparado (DSR).</span><span class="sxs-lookup"><span data-stu-id="aeaac-174">If **TRUE**, data outflow control is enabled when there is a data set ready (DSR) condition.</span></span> <span data-ttu-id="aeaac-175">DSR indica que los dispositivos de la conexión serie han establecido la conexión.</span><span class="sxs-lookup"><span data-stu-id="aeaac-175">DSR signals that the connection has been established by the devices on the serial connection.</span></span> <span data-ttu-id="aeaac-176">La transmisión de datos DSR se suspende hasta que se proporciona la señal DSR.</span><span class="sxs-lookup"><span data-stu-id="aeaac-176">DSR data transmission is suspended until the DSR signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-177">**DSRSensitivity**</span><span class="sxs-lookup"><span data-stu-id="aeaac-177">**DSRSensitivity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-178">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aeaac-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-180">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity")</span><span class="sxs-lookup"><span data-stu-id="aeaac-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDsrSensitivity")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-181">Si es **true**, el controlador de comunicaciones es sensible al estado de la señal DSR.</span><span class="sxs-lookup"><span data-stu-id="aeaac-181">If **TRUE**, the communications driver is sensitive to the state of the DSR signal.</span></span> <span data-ttu-id="aeaac-182">El controlador omite los bytes recibidos, a menos que la línea de entrada del módem DSR sea alta.</span><span class="sxs-lookup"><span data-stu-id="aeaac-182">The driver ignores any bytes received, unless the DSR modem input line is high.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-183">**DTRFlowControlType**</span><span class="sxs-lookup"><span data-stu-id="aeaac-183">**DTRFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeaac-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-186">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl")</span><span class="sxs-lookup"><span data-stu-id="aeaac-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDtrControl")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-187">Uso del control de flujo de terminal de datos preparado (DTR) una vez establecida una conexión.</span><span class="sxs-lookup"><span data-stu-id="aeaac-187">Use of the data terminal ready (DTR) flow control after a connection has been established.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="aeaac-188">**Habilitar** ("habilitar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-188">**Enable** ("Enable")</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="aeaac-189">**Deshabilitar** ("Deshabilitar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-189">**Disable** ("Disable")</span></span>


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="aeaac-190">**Protocolo de enlace** ("Protocolo de enlace")</span><span class="sxs-lookup"><span data-stu-id="aeaac-190">**Handshake** ("Handshake")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aeaac-191">**EOFCharacter**</span><span class="sxs-lookup"><span data-stu-id="aeaac-191">**EOFCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-192">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeaac-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-194">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-194">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EofChar")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-195">Valor del carácter que se usa para indicar el final de los datos.</span><span class="sxs-lookup"><span data-stu-id="aeaac-195">Value of the character used to signal the end of data.</span></span>

<span data-ttu-id="aeaac-196">Ejemplo: ^ Z</span><span class="sxs-lookup"><span data-stu-id="aeaac-196">Example: ^Z</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-197">**ErrorReplaceCharacter**</span><span class="sxs-lookup"><span data-stu-id="aeaac-197">**ErrorReplaceCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-198">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeaac-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-200">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-200">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-201">Valor del carácter que se utiliza para reemplazar los bytes recibidos con un error de paridad.</span><span class="sxs-lookup"><span data-stu-id="aeaac-201">Value of the character used to replace bytes received with a parity error.</span></span>

<span data-ttu-id="aeaac-202">Ejemplo: ^ C</span><span class="sxs-lookup"><span data-stu-id="aeaac-202">Example: ^C</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-203">**ErrorReplacementEnabled**</span><span class="sxs-lookup"><span data-stu-id="aeaac-203">**ErrorReplacementEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-204">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aeaac-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-206">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-207">Si **es true**, los bytes recibidos con errores de paridad se reemplazan por el valor de **ErrorReplaceCharacter** .</span><span class="sxs-lookup"><span data-stu-id="aeaac-207">If **TRUE**, bytes received with parity errors are replaced with the **ErrorReplaceCharacter** value.</span></span> <span data-ttu-id="aeaac-208">Los caracteres con errores de paridad solo se reemplazan si esta propiedad es **true** y la paridad está habilitada.</span><span class="sxs-lookup"><span data-stu-id="aeaac-208">Characters with parity errors are only replaced if this property is **TRUE** and the parity is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-209">**EventCharacter**</span><span class="sxs-lookup"><span data-stu-id="aeaac-209">**EventCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-210">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeaac-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-212">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EvtChar")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-213">Valor del carácter de control que se usa para señalar un evento, como el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="aeaac-213">Value of the control character that is used to signal an event, such as end of file.</span></span>

<span data-ttu-id="aeaac-214">Ejemplo: ^ e</span><span class="sxs-lookup"><span data-stu-id="aeaac-214">Example: ^e</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-215">**IsBusy**</span><span class="sxs-lookup"><span data-stu-id="aeaac-215">**IsBusy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-216">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aeaac-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-218">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| File Functions \| CreateFile")</span><span class="sxs-lookup"><span data-stu-id="aeaac-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-219">Si es **true**, el puerto serie está ocupado.</span><span class="sxs-lookup"><span data-stu-id="aeaac-219">If **TRUE**, the serial port is busy.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-220">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="aeaac-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeaac-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-223">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ DeviceMap \\ \\ SerialComm")</span><span class="sxs-lookup"><span data-stu-id="aeaac-223">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-224">Nombre del puerto serie de Windows.</span><span class="sxs-lookup"><span data-stu-id="aeaac-224">Name of the Windows serial port.</span></span>

<span data-ttu-id="aeaac-225">Ejemplo: "COM1"</span><span class="sxs-lookup"><span data-stu-id="aeaac-225">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-226">**Parity**</span><span class="sxs-lookup"><span data-stu-id="aeaac-226">**Parity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeaac-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-229">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Parity")</span><span class="sxs-lookup"><span data-stu-id="aeaac-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|Parity")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-230">Método de comprobación de la paridad que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="aeaac-230">Method of parity checking to be used.</span></span> <span data-ttu-id="aeaac-231">La paridad se utiliza como una técnica de comprobación de errores en la que se incluye un bit de paridad adicional con cada unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="aeaac-231">Parity is used as an error checking technique where an extra parity bit is included with every unit of data.</span></span> <span data-ttu-id="aeaac-232">A continuación, el receptor puede comprobar la validez de los datos contando los bits establecidos.</span><span class="sxs-lookup"><span data-stu-id="aeaac-232">The receiver can then verify the validity of the data by counting the bits that are set.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="aeaac-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** ("ninguno")</span><span class="sxs-lookup"><span data-stu-id="aeaac-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")</span></span>


</dt> <dd>

<span data-ttu-id="aeaac-234">No se utiliza la comprobación de paridad.</span><span class="sxs-lookup"><span data-stu-id="aeaac-234">Parity checking not used.</span></span>

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="aeaac-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Impar** ("impar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Odd** ("Odd")</span></span>


</dt> <dd>

<span data-ttu-id="aeaac-236">Establece el bit de paridad de forma que el recuento de bits establecidos sea un número impar.</span><span class="sxs-lookup"><span data-stu-id="aeaac-236">Sets the parity bit so that the count of bits set is an odd number.</span></span>

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="aeaac-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Par** ("incluso")</span><span class="sxs-lookup"><span data-stu-id="aeaac-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Even** ("Even")</span></span>


</dt> <dd>

<span data-ttu-id="aeaac-238">Establece el bit de paridad de forma que el recuento de bits establecidos sea un número par.</span><span class="sxs-lookup"><span data-stu-id="aeaac-238">Sets the parity bit so that the count of bits set is an even number.</span></span>

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span data-ttu-id="aeaac-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Marcar** ("marcar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")</span></span>


</dt> <dd>

<span data-ttu-id="aeaac-240">Establece el conjunto de bits de paridad en 1.</span><span class="sxs-lookup"><span data-stu-id="aeaac-240">Leaves the parity bit set to 1.</span></span>

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span data-ttu-id="aeaac-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Espacio** ("espacio")</span><span class="sxs-lookup"><span data-stu-id="aeaac-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Space** ("Space")</span></span>


</dt> <dd>

<span data-ttu-id="aeaac-242">Deja el bit de paridad establecido en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="aeaac-242">Leaves the parity bit set to 0 (zero).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aeaac-243">**ParityCheckEnabled**</span><span class="sxs-lookup"><span data-stu-id="aeaac-243">**ParityCheckEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-244">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aeaac-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-246">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity")</span><span class="sxs-lookup"><span data-stu-id="aeaac-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fParity")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-247">Si es **true**, se habilita la comprobación de paridad.</span><span class="sxs-lookup"><span data-stu-id="aeaac-247">If **TRUE**, parity checking is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-248">**RTSFlowControlType**</span><span class="sxs-lookup"><span data-stu-id="aeaac-248">**RTSFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeaac-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-251">Solicitud de envío (RTS) de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="aeaac-251">Request to send (RTS) flow control.</span></span> <span data-ttu-id="aeaac-252">RTS se utiliza para indicar que los datos están disponibles para la transmisión.</span><span class="sxs-lookup"><span data-stu-id="aeaac-252">RTS is used to signal that data is available for transmission.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="aeaac-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Habilitar** ("habilitar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** ("Enable")</span></span>


</dt> <dd>

<span data-ttu-id="aeaac-254">Se deja RTS en la sesión de transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="aeaac-254">RTS is left on for the data transfer session.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="aeaac-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deshabilitar** ("Deshabilitar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** ("Disable")</span></span>


</dt> <dd>

<span data-ttu-id="aeaac-256">Se omite RTS después de recibir la primera señal RTS.</span><span class="sxs-lookup"><span data-stu-id="aeaac-256">RTS is ignored after the first RTS signal is received.</span></span>

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="aeaac-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Protocolo de enlace** ("Protocolo de enlace")</span><span class="sxs-lookup"><span data-stu-id="aeaac-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")</span></span>


</dt> <dd>

<span data-ttu-id="aeaac-258">Se desactiva RTS si el búfer de transmisión tiene más de tres trimestres, y se activa RTS cuando el búfer está por debajo de la mitad.</span><span class="sxs-lookup"><span data-stu-id="aeaac-258">RTS is turned off if the transmission buffer is more than three-quarters full, and RTS is turned on when the buffer is less than one-half full.</span></span>

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span data-ttu-id="aeaac-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Alternancia** ("alternancia")</span><span class="sxs-lookup"><span data-stu-id="aeaac-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Toggle** ("Toggle")</span></span>


</dt> <dd>

<span data-ttu-id="aeaac-260">RTS se activa si hay datos almacenados en búfer para la transmisión.</span><span class="sxs-lookup"><span data-stu-id="aeaac-260">RTS is turned on if there is any data buffered for transmission.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aeaac-261">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="aeaac-261">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-262">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeaac-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-264">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="aeaac-264">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-265">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="aeaac-265">Identifier by which the current object is known.</span></span>

<span data-ttu-id="aeaac-266">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="aeaac-266">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-267">**StopBits**</span><span class="sxs-lookup"><span data-stu-id="aeaac-267">**StopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-268">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeaac-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-270">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| parada")</span><span class="sxs-lookup"><span data-stu-id="aeaac-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|StopBits")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-271">Número de bits de parada que se usarán.</span><span class="sxs-lookup"><span data-stu-id="aeaac-271">Number of stop bits to be used.</span></span> <span data-ttu-id="aeaac-272">Los bits de parada separan cada unidad de datos en una conexión serie asincrónica.</span><span class="sxs-lookup"><span data-stu-id="aeaac-272">Stop bits separate each unit of data on an asynchronous serial connection.</span></span> <span data-ttu-id="aeaac-273">También se envían continuamente cuando no hay datos disponibles para la transmisión.</span><span class="sxs-lookup"><span data-stu-id="aeaac-273">They are also sent continuously when no data is available for transmission.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="aeaac-274">**1** ("1")</span><span class="sxs-lookup"><span data-stu-id="aeaac-274">**1** ("1")</span></span>


</dt> <dd></dd> <dt>

<span id="1.5"></span>

<span data-ttu-id="aeaac-275">**1,5** ("1,5")</span><span class="sxs-lookup"><span data-stu-id="aeaac-275">**1.5** ("1.5")</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="aeaac-276">**2** ("2")</span><span class="sxs-lookup"><span data-stu-id="aeaac-276">**2** ("2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aeaac-277">**XOffCharacter**</span><span class="sxs-lookup"><span data-stu-id="aeaac-277">**XOffCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-278">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeaac-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-280">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffChar")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-281">Valor del carácter XOFF para la transmisión y la recepción.</span><span class="sxs-lookup"><span data-stu-id="aeaac-281">Value of the XOFF character for both transmission and reception.</span></span> <span data-ttu-id="aeaac-282">XOFF es un control de software para detener la transmisión de datos (mientras que RTS y CTS son controles de hardware).</span><span class="sxs-lookup"><span data-stu-id="aeaac-282">XOFF is a software control to stop the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="aeaac-283">XON reanuda la transmisión.</span><span class="sxs-lookup"><span data-stu-id="aeaac-283">XON resumes the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-284">**XOffXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="aeaac-284">**XOffXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-285">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeaac-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-287">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim")</span><span class="sxs-lookup"><span data-stu-id="aeaac-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffLim")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-288">Número máximo de bytes permitidos en el búfer de entrada antes de que se envíe el carácter XOFF.</span><span class="sxs-lookup"><span data-stu-id="aeaac-288">Maximum number of bytes allowed in the input buffer before the XOFF character is sent.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-289">**XOnCharacter**</span><span class="sxs-lookup"><span data-stu-id="aeaac-289">**XOnCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-290">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeaac-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-292">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar")</span><span class="sxs-lookup"><span data-stu-id="aeaac-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonChar")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-293">Valor del carácter XON para la transmisión y la recepción.</span><span class="sxs-lookup"><span data-stu-id="aeaac-293">Value of the XON character for both transmission and reception.</span></span> <span data-ttu-id="aeaac-294">XON es un control de software para reanudar la transmisión de datos (mientras que RTS y CTS son controles de hardware).</span><span class="sxs-lookup"><span data-stu-id="aeaac-294">XON is a software control to resume the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="aeaac-295">XOFF detiene la transmisión.</span><span class="sxs-lookup"><span data-stu-id="aeaac-295">XOFF stops the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-296">**XOnXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="aeaac-296">**XOnXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-297">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeaac-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-299">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim")</span><span class="sxs-lookup"><span data-stu-id="aeaac-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonLim")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-300">Número mínimo de bytes permitidos en el búfer de entrada antes de que se envíe el carácter XON.</span><span class="sxs-lookup"><span data-stu-id="aeaac-300">Minimum number of bytes allowed in the input buffer before the XON character is sent.</span></span> <span data-ttu-id="aeaac-301">Esta propiedad funciona junto con **XOffXmitThreshold** para regular la velocidad a la que se transfieren los datos.</span><span class="sxs-lookup"><span data-stu-id="aeaac-301">This property works in conjunction with **XOffXMitThreshold** to regulate the rate at which data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="aeaac-302">**XOnXOffInFlowControl**</span><span class="sxs-lookup"><span data-stu-id="aeaac-302">**XOnXOffInFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-303">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeaac-303">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-305">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX")</span><span class="sxs-lookup"><span data-stu-id="aeaac-305">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fInX")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-306">Si es **true**, el control de flujo XON/XOFF se usa durante la recepción.</span><span class="sxs-lookup"><span data-stu-id="aeaac-306">If **TRUE**, XON/XOFF flow control is used during reception.</span></span> <span data-ttu-id="aeaac-307">Si es **true**, el valor **XOffCharacter** se envía cuando el búfer de entrada se encuentra en **XOffXmitThreshold** bytes de llenado y se envía el valor **XOnCharacter** cuando el búfer de entrada se encuentra dentro de **XOnXMitThreshold** bytes de estar vacíos.</span><span class="sxs-lookup"><span data-stu-id="aeaac-307">If **TRUE**, the **XOffCharacter** value is sent when the input buffer comes within **XOffXMitThreshold** bytes of being full, and the **XOnCharacter** value is sent when the input buffer comes within **XOnXMitThreshold** bytes of being empty.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="aeaac-308"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="aeaac-308"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="aeaac-309">false</span><span class="sxs-lookup"><span data-stu-id="aeaac-309">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="aeaac-310"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="aeaac-310"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="aeaac-311">TRUE</span><span class="sxs-lookup"><span data-stu-id="aeaac-311">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aeaac-312">**XOnXOffOutFlowControl**</span><span class="sxs-lookup"><span data-stu-id="aeaac-312">**XOnXOffOutFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeaac-313">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aeaac-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeaac-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeaac-315">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX")</span><span class="sxs-lookup"><span data-stu-id="aeaac-315">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutX")</span></span>
</dt> </dl>

<span data-ttu-id="aeaac-316">**XOnXOffOutFlowControl** especifica si se utiliza el control de flujo XON o XOFF durante la transmisión.</span><span class="sxs-lookup"><span data-stu-id="aeaac-316">The **XOnXOffOutFlowControl** specifies whether XON or XOFF flow control is used during transmission.</span></span> <span data-ttu-id="aeaac-317">Si es **true**, la transmisión se detiene cuando se recibe el valor **XOffCharacter** y se inicia de nuevo cuando se recibe el valor **XOnCharacter** .</span><span class="sxs-lookup"><span data-stu-id="aeaac-317">If **TRUE**, transmission stops when the **XOffCharacter** value is received and starts again when the **XOnCharacter** value is received.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aeaac-318">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aeaac-318">Remarks</span></span>

<span data-ttu-id="aeaac-319">La **clase \_ SerialPortConfiguration de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="aeaac-319">The **Win32\_SerialPortConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aeaac-320">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeaac-320">Requirements</span></span>



| <span data-ttu-id="aeaac-321">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeaac-321">Requirement</span></span> | <span data-ttu-id="aeaac-322">Value</span><span class="sxs-lookup"><span data-stu-id="aeaac-322">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeaac-323">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aeaac-323">Minimum supported client</span></span><br/> | <span data-ttu-id="aeaac-324">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aeaac-324">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aeaac-325">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aeaac-325">Minimum supported server</span></span><br/> | <span data-ttu-id="aeaac-326">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aeaac-326">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aeaac-327">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aeaac-327">Namespace</span></span><br/>                | <span data-ttu-id="aeaac-328">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aeaac-328">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aeaac-329">MOF</span><span class="sxs-lookup"><span data-stu-id="aeaac-329">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aeaac-330"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aeaac-330"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aeaac-331">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aeaac-331">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeaac-332"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeaac-332"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeaac-333">Vea también</span><span class="sxs-lookup"><span data-stu-id="aeaac-333">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeaac-334">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="aeaac-334">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="aeaac-335">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="aeaac-335">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

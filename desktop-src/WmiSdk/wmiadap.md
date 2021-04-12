---
description: Wmiadap es una aplicación que se ejecuta en Windows y que puede actualizar la información de rendimiento en el repositorio WMI.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5d2de65e8566283b341c5af52048cc79cc0299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279278"
---
# <a name="wmiadap"></a>wmiadap

Wmiadap es una aplicación que se ejecuta en Windows y que puede actualizar la información de rendimiento en el repositorio WMI. Por lo general, esto permite a los desarrolladores y administradores de ti crear scripts que tengan acceso a información de rendimiento, como la cantidad de memoria utilizada por una aplicación. En el siguiente tema se describe la interfaz de la línea de comandos que puede usar para controlar cómo wmiadap recupera la información.

Wmiadap se instala con el sistema operativo en la mayoría de los sistemas, en el directorio C: \\ Windows \\ system32 \\ WBEM. Si ve mensajes de error relacionados con wmiadap.exe, busque [soporte técnico de Microsoft](https://support.microsoft.com/). Por lo general, no debe eliminar wmiadap.exe del sistema, a menos que se indique lo contrario.

La transferencia de datos de las bibliotecas de rendimiento y la actualización de clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) se realiza mediante los proveedores [WmiPerfClass](wmi-providers.md) y [WMIPerfInst](wmi-providers.md) . El proveedor WmiPerfClass actualiza [las clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes) de WMI solo cuando se agrega un nuevo objeto de rendimiento. Todavía puede ejecutar Wmiadap con el modificador **/r** para analizar los controladores de modelo de controlador de Windows para crear objetos de rendimiento. El modificador **/f** todavía fuerza una actualización de las clases WMI de las bibliotecas de rendimiento.

Los siguientes modificadores están disponibles en el símbolo del sistema.

**wmiadap** \[  \] /f \[ **/r**\]

## <a name="switches"></a>Conmutadores

<dl> <dt>

<span id="_f"></span><span id="_F"></span>**/f**
</dt> <dd>

Analiza todas las bibliotecas de rendimiento en el sistema y actualiza las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Analiza todos los controladores de Modelo de controlador de Windows del sistema para crear objetos de rendimiento.

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[Bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[**WinMgmt**](winmgmt.md)
</dt> </dl>

 

 

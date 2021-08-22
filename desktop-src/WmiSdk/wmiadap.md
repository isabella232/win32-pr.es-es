---
description: Wmiadap es una aplicación que se ejecuta en Windows que puede actualizar la información de rendimiento en el repositorio WMI.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a58de2ca5e678cbbb99f803415572be236f2a545ed149b9ad598fb7f9a4664
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049843"
---
# <a name="wmiadap"></a>wmiadap

Wmiadap es una aplicación que se ejecuta en Windows que puede actualizar la información de rendimiento en el repositorio WMI. Por lo general, esto permite a los desarrolladores y administradores de TI crear scripts que acceden a información de rendimiento, como la cantidad de memoria que usa una aplicación. En el tema siguiente se describe la interfaz de línea de comandos que puede usar para controlar cómo wmiadap recupera información.

Wmiadap se instala con el sistema operativo en la mayoría de los sistemas, en el directorio C: \\ Windows \\ System32 \\ wbem. Si ve mensajes de error relacionados con wmiadap.exe, busque [Soporte técnico de Microsoft](https://support.microsoft.com/). Por lo general, no debe eliminar wmiadap.exe del sistema, a menos que se indique lo contrario.

La transferencia de datos de las bibliotecas de rendimiento y la actualización de clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) se realiza mediante los proveedores [WmiPerfClass](wmi-providers.md) y [WMIPerfInst.](wmi-providers.md) El proveedor WmiPerfClass actualiza las clases [de](/windows/desktop/CIMWin32Prov/performance-counter-classes) contador de rendimiento wmi solo cuando se agrega un nuevo objeto de rendimiento. Todavía puede ejecutar Wmiadap con el modificador **/r** para analizar los controladores Windows Driver Model para crear objetos de rendimiento. El **modificador /f** sigue obligando a actualizar las clases WMI de las bibliotecas de rendimiento.

Los modificadores siguientes están disponibles en el símbolo del sistema.

**wmiadap** \[ **/f** \] \[ **/r**\]

## <a name="switches"></a>Modificadores

<dl> <dt>

<span id="_f"></span><span id="_F"></span>**/f**
</dt> <dd>

Analiza todas las bibliotecas de rendimiento del sistema y actualiza las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Analiza todos los controladores Windows driver model del sistema para crear objetos de rendimiento.

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[Bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[**Winmgmt**](winmgmt.md)
</dt> </dl>

 

 

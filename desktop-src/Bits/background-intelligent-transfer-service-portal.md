---
title: Servicio de transferencia inteligente en segundo plano
description: El Servicio de transferencia inteligente en segundo plano (BITS) transfiere archivos (descargas o cargas) entre un cliente y un servidor, y proporciona información sobre el progreso de las transferencias.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Servicio de transferencia inteligente en segundo plano
- Servicio de transferencia inteligente en segundo plano, página de inicio
- BITS (vea Servicio de transferencia inteligente en segundo plano)
- descargar BITS de archivos
- BITS de transferencia de archivo en segundo plano
- cargar BITS de archivos
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: a531821665490735b391ab2714f5b37146c6bc1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995502"
---
# <a name="background-intelligent-transfer-service"></a>Servicio de transferencia inteligente en segundo plano

## <a name="purpose"></a>Propósito

Los programadores y los administradores del sistema usan Servicio de transferencia inteligente en segundo plano (BITS) para descargar archivos o cargar archivos en los servidores Web HTTP y los recursos compartidos de archivos SMB. BITS tendrá en cuenta el costo de la transferencia, así como el uso de la red para que el trabajo en primer plano del usuario tenga el menor impacto posible. BITS también controla la interuptions de red, la pausa y la reanudación automática de las transferencias, incluso después de un reinicio. BITS incluye cmdlets de PowerShell para crear y administrar transferencias, así como la utilidad de línea de comandos BitsAdmin.

> [!Note]  
> Windows puede usar BITS para descargar actualizaciones en el sistema local. Si es un usuario final que busca maneras de solucionar problemas de la instalación de BITS, consulte [solución de problemas de Windows Update](https://support.microsoft.com/help/10164/fix-windows-update-errors). 
 

## <a name="where-applicable"></a>Donde sea aplicable

Use BITS para las aplicaciones que necesitan:

-   Descargue o cargue archivos en un servidor Web HTTP o REST o en un servidor de archivos SMB.
-   Reanudar automáticamente las transferencias de archivos después de desconectarse de la red y reiniciar el equipo.
-   Conservar la capacidad de respuesta de otras aplicaciones de red.
-   Tenga en cuentan el costo de red en, por ejemplo, las redes móviles
-   Opcionalmente, puede trabajar con [BranchCache](/windows-server/networking/branchcache/branchcache) para optimizar el tráfico de la red de área extensa (WAN).

## <a name="developer-audience"></a>Audiencia de desarrolladores

BITS es una interfaz COM diseñada para desarrolladores de C y C++ que los desarrolladores de .NET también pueden usar. Los desarrolladores de UWP deben usar la API [Windows. networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) y no la API de bits.

## <a name="bits-versions"></a>Versiones de BITS

Para obtener el historial de versiones completo e información sobre el sistema operativo anterior, vea [novedades](what-s-new.md).


## <a name="in-this-section"></a>En esta sección



| Tema                                                           | Descripción                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de BITS](about-bits.md)<br/>                         | Información general sobre BITS.<br/>                                                                                                                                      |
| [Usar BITS](using-bits.md)<br/>                         | Guía de procedimientos para desarrollar clientes de BITS que transfieren archivos entre un cliente y un servidor.<br/>                                                                        |
| [Referencia de BITS](bits-reference.md)<br/>                 | Información de referencia de las interfaces de programación de BITS. También contiene información sobre ejemplos, herramientas, configuración del servidor para trabajos de carga y el protocolo de carga.<br/> |
| [Procedimientos recomendados](best-practices-when-using-bits.md)<br/> | Información que se debe tener en cuenta al diseñar una aplicación que usa BITS.<br/>                                                                                                |



 

## <a name="additional-resources"></a>Recursos adicionales

Los siguientes son recursos adicionales.


|             |                                                                                                                                                 |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL de referencia de .NET   | Para obtener información sobre el uso de BITS desde .NET mediante el uso de archivos dll de referencia, consulte [llamar a bits desde .net mediante archivos dll de referencia](/windows/desktop/Bits/bits-dot-net)      |
| Contenedor .NET   | En el caso de otros contenedores de .NET para BITS, puede buscar en [Nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) los proyectos etiquetados con la etiqueta bits.        |



 

 


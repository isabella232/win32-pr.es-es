---
description: Los conjuntos de API son grupos funcionales de las API de Win32 en el sistema operativo principal. Proporcionan una separación arquitectónica del archivo DLL del host en el que se define una API win32 determinada y el grupo funcional al que pertenece la API.
title: Windows Conjuntos de API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 34724f255b963c23406ed5bdc59de0278e68a6f75de0d00b4d45aa449575af89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737612"
---
# <a name="windows-api-sets"></a>Windows Conjuntos de API

Todas las versiones de Windows 10 comparten una base común de componentes del sistema operativo que se denomina sistema operativo principal *(en* algunos contextos, esta base común también se *denomina OneCore*). En los componentes principales del sistema operativo, las API de Win32 se organizan en grupos funcionales denominados *conjuntos de API.*

El propósito de un conjunto de API es proporcionar una separación arquitectónica del archivo DLL del host en el que se implementa una API win32 determinada y el contrato funcional al que pertenece la API. El desacobado que proporcionan los conjuntos de API entre la implementación y los contratos ofrece muchas ventajas de ingeniería para los desarrolladores. En concreto, el uso de conjuntos de API en el código puede mejorar la compatibilidad con todos los Windows 10 dispositivos.

Los conjuntos de API abordan específicamente los escenarios siguientes:

- Aunque la amplitud completa de la API Win32 se admite en equipos, solo un subconjunto de la API win32 está disponible en otros dispositivos de Windows 10 como HoloLens, Xbox y otros dispositivos que se ejecutan Windows 10 veces. El nombre del conjunto de API proporciona un mecanismo de consulta para detectar correctamente si una API está disponible en un dispositivo determinado.

- Algunas implementaciones de api Win32 existen en archivos DLL con nombres diferentes en diferentes Windows 10 dispositivos. El uso de nombres de conjunto de API en lugar de nombres de DLL al detectar la disponibilidad de la API y retrasar la carga de las API proporciona una ruta correcta a la implementación independientemente de dónde se implemente realmente la API.

Para más información, consulte Operación del [cargador de conjuntos de API y](api-set-loader-operation.md) [Detección de disponibilidad del conjunto de API.](detect-api-set-availability.md)

## <a name="linking-to-umbrella-libraries"></a>Vinculación a bibliotecas de paraguas

Para facilitar la restricción del código a las API de Win32 que se admiten en el sistema operativo principal, se proporciona una serie de *bibliotecas paraguas*. Por ejemplo, una biblioteca de paraguas denominada OneCore.lib proporciona las exportaciones para el subconjunto de API de Win32 que son comunes a todos los Windows 10 dispositivos.

Las API de una biblioteca de paraguas se pueden implementar en una variedad de módulos. La biblioteca de paraguas abstrae esos detalles de usted, lo que hace que el código sea más portátil en Windows 10 y dispositivos. En lugar de vincular a bibliotecas como kernel32.lib y advapi32.lib, basta con vincular la aplicación de escritorio o el controlador con la biblioteca de paraguas que contiene el conjunto de API básicas del sistema operativo que le interesan.

Para obtener más información, [vea Windows bibliotecas de paraguas](windows-umbrella-libraries.md).

## <a name="api-set-contract-names"></a>Nombres de contrato del conjunto de API

Los conjuntos de API se identifican mediante un nombre de contrato sólido que sigue estas convenciones estándar reconocidas por el cargador de bibliotecas. 

- El nombre debe comenzar con la **cadena api-** o **ext-**. 
    - Los nombres que comienzan **por api representan** las API que se garantiza que existen en todas Windows 10 versiones.
    - Los nombres que **comienzan por ext-** representan las API que pueden no existir en todas las Windows 10 versiones.
- El nombre debe terminar con la secuencia **l \<n\> - \<n\> - \<n\>**, donde **n** consta de dígitos decimales.
- El cuerpo del nombre puede ser caracteres alfanuméricos o guiones ( **-** ).
- El nombre distingue mayúsculas de minúsculas.

Estos son algunos ejemplos de nombres de contrato de conjunto de API:

- **api-ms-win-core-ums-l1-1-0**
- **ext-ms-win-com-ole32-l1-1-5**
- **ext-ms-win-ntuser-window-l1-1-0**
- **ext-ms-win-ntuser-window-l1-1-1**

Puede usar un nombre de conjunto de API en el contexto de una operación de cargador como [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [P/Invoke](/dotnet/standard/native-interop/pinvoke) en lugar de un nombre de módulo DLL para garantizar una ruta correcta a la implementación independientemente de dónde se implemente realmente la API en el dispositivo actual. Sin embargo, al hacerlo, debe anexar la cadena **.dll** al final del nombre del contrato. Este es un requisito del cargador para funcionar correctamente y no se considera realmente una parte del nombre del contrato. Aunque los nombres de contrato son similares a los nombres de DLL en este contexto, son fundamentalmente diferentes de los nombres de módulo DLL y no hacen referencia directamente a un archivo en disco.

Excepto para anexar la cadena **.dll** operaciones del cargador, los nombres de contrato del conjunto de API deben considerarse un identificador inmutable que corresponde a una versión de contrato específica.

## <a name="identifying-api-sets-for-win32-apis"></a>Identificación de conjuntos de API para las API de Win32

Para identificar si una API win32 determinada pertenece a un conjunto de API, revise la tabla de requisitos de la documentación de referencia de la API. Si la API pertenece a un conjunto de API, en la tabla de requisitos del artículo se enumeran el nombre del conjunto de API y la versión de Windows en la que la API se introdujo por primera vez en el conjunto de API. Para obtener ejemplos de API que pertenecen a un conjunto de API, consulte estos artículos:

- [AllowSetForegroundWindow](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow)
- [FindWindowsEx](/windows/win32/api/winuser/nf-winuser-findwindowexa)
- [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile)

## <a name="in-this-section"></a>En esta sección

* [Operación de cargador del conjunto de API](api-set-loader-operation.md)
* [Detección de disponibilidad del conjunto de API](detect-api-set-availability.md)
* [Bibliotecas de paraguas de Windows](windows-umbrella-libraries.md)
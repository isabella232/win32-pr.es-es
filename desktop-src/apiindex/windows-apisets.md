---
description: Los conjuntos de API son grupos funcionales de las API de Win32 en el sistema operativo principal. Proporcionan una separación arquitectónica de la DLL de host en la que se define una API de Win32 determinada y el grupo funcional al que pertenece la API.
title: Conjuntos de API de Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 15c8e6ad8124abf06e6ab3c2a8ca2bcd83772855
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104488615"
---
# <a name="windows-api-sets"></a>Conjuntos de API de Windows

Todas las versiones de Windows 10 comparten una base común de componentes del sistema operativo que se denomina *sistema operativo principal* (en algunos contextos, esta base común también se denomina *OneCore*). En los componentes principales del sistema operativo, las API de Win32 están organizadas en grupos funcionales denominados *conjuntos de API*.

El propósito de un conjunto de API es proporcionar una separación arquitectónica de la DLL de host en la que se implementa una API de Win32 determinada y el contrato funcional al que pertenece la API. El desacoplamiento que proporcionan los conjuntos de API entre la implementación y los contratos ofrece muchas ventajas de ingeniería para los desarrolladores. En concreto, el uso de conjuntos de API en el código puede mejorar la compatibilidad con todos los dispositivos de Windows 10.

Los conjuntos de API abordan específicamente los escenarios siguientes:

- Aunque el alcance completo de la API de Win32 es compatible con los equipos, solo hay un subconjunto de la API de Win32 disponible en otros dispositivos con Windows 10, como HoloLens, Xbox y otros dispositivos que ejecutan Windows 10X. El nombre del conjunto de API proporciona un mecanismo de consulta para detectar correctamente si una API está disponible en cualquier dispositivo determinado.

- Algunas implementaciones de API de Win32 existen en archivos DLL con nombres diferentes en distintos dispositivos de Windows 10. El uso de nombres de conjuntos de API en lugar de nombres de DLL al detectar la disponibilidad de API y retrasar la carga de API proporcionan una ruta correcta a la implementación independientemente de dónde se implemente realmente la API.

Para obtener más información, consulte [operación del cargador de conjunto de API](api-set-loader-operation.md) y [detectar disponibilidad del conjunto de API](detect-api-set-availability.md).

## <a name="linking-to-umbrella-libraries"></a>Vincular a bibliotecas de paraguas

Para facilitar la restricción del código a las API de Win32 que se admiten en el sistema operativo principal, se proporciona una serie de *bibliotecas de paraguas*. Por ejemplo, una biblioteca de paraguas denominada OneCore. lib proporciona las exportaciones para el subconjunto de las API de Win32 que son comunes a todos los dispositivos de Windows 10.

Las API de una biblioteca paraguas se pueden implementar en un intervalo de módulos. La biblioteca de paraguas abstrae esos detalles, lo que hace que el código sea más portátil entre las versiones y los dispositivos de Windows 10. En lugar de vincular a bibliotecas como Kernel32. lib y advapi32. lib, simplemente vincule la aplicación de escritorio o el controlador con la biblioteca de paraguas que contiene el conjunto de API principales del sistema operativo que le interesan.

Para obtener más información, consulte [bibliotecas de paraguas de Windows](windows-umbrella-libraries.md).

## <a name="api-set-contract-names"></a>Nombres de contrato del conjunto de API

Los conjuntos de API se identifican mediante un nombre de contrato seguro que sigue estas convenciones estándar reconocidas por el cargador de la biblioteca. 

- El nombre debe comenzar con la **API de cadena-** o **ext-**. 
    - Los nombres que comienzan por **API-** representan las API que se garantiza que existen en todas las versiones de Windows 10.
    - Nombres que comienzan por **EXT:** representan API que pueden no existir en todas las versiones de Windows 10.
- El nombre debe terminar con la secuencia **l \<n\> - \<n\> - \<n\>**, donde **n** consta de dígitos decimales.
- El cuerpo del nombre puede ser caracteres alfanuméricos o guiones ( **-** ).
- El nombre distingue mayúsculas de minúsculas.

Estos son algunos ejemplos de nombres de contrato de conjunto de API:

- **API-MS-WIN-Core-UMS-L1-1-0**
- **EXT-MS-WIN-com-ole32-L1-1-5**
- **EXT-MS-WIN-Ntuser-Window-L1-1-0**
- **EXT-MS-WIN-Ntuser-Window-L1-1-1**

Puede usar un nombre de conjunto de API en el contexto de una operación de cargador como [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [P/Invoke](/dotnet/standard/native-interop/pinvoke) en lugar de un nombre de módulo DLL para garantizar una ruta correcta a la implementación, independientemente de dónde se implemente realmente la API en el dispositivo actual. Sin embargo, cuando lo haga, debe anexar el **archivo String. dll** al final del nombre del contrato. Este es un requisito del cargador para que funcione correctamente y no se considera realmente una parte del nombre del contrato. Aunque los nombres de contrato aparecen de forma similar a los nombres de los archivos DLL en este contexto, son fundamentalmente diferentes de los nombres de los módulos DLL y no hacen referencia directa a un archivo en el disco.

A excepción de anexar el **archivo String. dll** en las operaciones del cargador, los nombres de contrato del conjunto de API se deben considerar como un identificador inmutable que se corresponda con una versión específica del contrato.

## <a name="identifying-api-sets-for-win32-apis"></a>Identificación de los conjuntos de API para las API Win32

Para identificar si una API de Win32 determinada pertenece a un conjunto de API, revise la tabla de requisitos en la documentación de referencia de la API. Si la API pertenece a un conjunto de API, la tabla de requisitos del artículo enumera el nombre del conjunto de API y la versión de Windows en la que se presentó la API por primera vez en el conjunto de API. Para obtener ejemplos de las API que pertenecen a un conjunto de API, consulte estos artículos:

- [AllowSetForegroundWindow](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow)
- [FindWindowsEx](/windows/win32/api/winuser/nf-winuser-findwindowexa)
- [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile)

## <a name="in-this-section"></a>En esta sección

* [Operación de cargador del conjunto de API](api-set-loader-operation.md)
* [Detección de disponibilidad del conjunto de API](detect-api-set-availability.md)
* [Bibliotecas de paraguas de Windows](windows-umbrella-libraries.md)
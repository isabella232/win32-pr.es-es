---
description: El ejemplo de código SearchEvents muestra cómo dar prioridad a los eventos de indexación.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: SearchEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363234"
---
# <a name="searchevents"></a>SearchEvents

El ejemplo de código SearchEvents muestra cómo dar prioridad a los eventos de indexación.

En este tema se incluyen las siguientes secciones.

- [Requisitos](#requirements)
- [Descargar el ejemplo](#downloading-the-sample)
- [Compilar el ejemplo](#building-the-sample)
- [Ejecución del ejemplo](#running-the-sample)
- [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos

| Producto     | Versión del producto          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 o 10    |
| Windows SDK | 7.0 o superior           |

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en la siguiente ubicación.

| Location      | Dirección URL de ruta de acceso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [Ejemplo de SearchEvents](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> Para todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.

## <a name="building-the-sample"></a>Generar el ejemplo

1. Abra Windows Explorador de eventos y vaya al **directorio del proyecto SearchEvents.**
2. Haga doble clic en el icono del archivo Eventing.sln para abrir el proyecto en Visual Studio.
  
    > [!NOTE]  
    > El archivo sln se creó en una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior. Esto no afectará al comportamiento de la muestra.

3. En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1. Vaya al directorio que contiene el nuevo ejecutable, mediante la ventana símbolo del sistema o Windows Explorador.
2. En el símbolo del sistema, escriba o, en Windows Explorer, haga doble clic en el `Eventing.exe` icono para Eventing.exe.

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[**NIVEL DE \_ PRIORIDAD**](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[**TIPO DE EVENTO \_ ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a>Otros ejemplos

[Ejemplos de código de búsqueda](-search-samples-ovw.md)

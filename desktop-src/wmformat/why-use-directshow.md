---
title: ¿Por qué usar DirectShow
description: ¿Por qué usar DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows SDK de formato multimedia, DirectShow
- Windows SDK de formato multimedia, hardware
- Windows SDK de formato multimedia, Windows Driver Model (WDM)
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- Formato de sistemas avanzados (ASF), hardware
- ASF (formato de sistemas avanzados), hardware
- Advanced Systems Format (ASF),Windows Driver Model (WDM)
- ASF (formato de sistemas avanzados), Windows driver model (WDM)
- DirectShow,about
- DirectShow,hardware
- DirectShow,Windows driver model (WDM)
- Windows Modelo de controlador (WDM)
- WDM (Windows driver model)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247220"
---
# <a name="why-use-directshow"></a>¿Por qué usar DirectShow?

Hay dos razones principales por las que una aplicación podría usar DirectShow en lugar del SDK de formato multimedia de Windows directamente: para la comodidad de la arquitectura de streaming de DirectShow y para el acceso al hardware.

## <a name="convenience"></a>Comodidad

Con DirectShow de streaming, solo se necesitan algunas llamadas de método para reproducir Windows multimedia o Windows de vídeo multimedia. También se simplifica la creación de archivos. Basta con especificar un perfil mediante la interfaz **IConfigAsfWriter** en el filtro y DirectShow carga automáticamente los componentes necesarios para representar o escribir las secuencias, y proporciona los mecanismos para transferir y sincronizar el flujo de datos multimedia. DirectShow es especialmente útil al convertir contenido de formatos variados a Windows formato multimedia. Puede crear gráficos de DirectShow que descodifican una amplia variedad de tipos de archivo y compresión y, a continuación, alimentar las secuencias descodificadas en el filtro [WM ASF Writer.](wm-asf-writer-filter.md) En comparación, el ejemplo UncompAVItoWMV de este SDK solo funciona con archivos AVI sin comprimir. Las secuencias de texto y los flujos de datos arbitrarios también se pueden crear o representar a través de DirectShow, pero esto puede requerir que se creen filtros de DirectShow personalizados para procesar esos flujos.

## <a name="access-to-hardware"></a>Acceso al hardware

DirectShow es la única manera de que el código de la aplicación acceda a dispositivos de hardware basados en el modelo de controlador de Windows (WDM), como cámaras DV 1394, tuneres de TV y cámaras web USB. Si la aplicación debe capturar datos directamente desde un dispositivo de hardware basado en WDM y transcodificarlo en formato multimedia de Windows y el SDK de codificador multimedia de Windows no se adapta a sus necesidades, DirectShow es la única alternativa. DirectShow también se puede usar para acceder a dispositivos heredados basados en Video para Windows.

 

 





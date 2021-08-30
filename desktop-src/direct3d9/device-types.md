---
description: Tipos de dispositivo (Direct3D 9)
ms.assetid: 860f3de2-beaf-4df1-82d0-a4b7508156c2
title: Tipos de dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c0ba90ffe4e80a99805f10e77246f1c8e11dec39f3ff1160577fbb2e2d9628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952205"
---
# <a name="device-types-direct3d-9"></a>Tipos de dispositivo (Direct3D 9)

## <a name="hal-device"></a>Dispositivo DESALTE

El tipo de dispositivo principal es el dispositivo ya existente, que admite la rasterización acelerada por hardware y el procesamiento de vértices de hardware y software. Si el equipo en el que se ejecuta la aplicación está equipado con un adaptador de pantalla compatible con Direct3D, la aplicación debe usarla para las operaciones de Direct3D. Los dispositivos Direct3D implementan todos o parte de los módulos de transformación, iluminación y rasterización en el hardware.

Las aplicaciones no tienen acceso directo a los adaptadores de gráficos. Llaman a funciones y métodos de Direct3D. Direct3D accede al hardware a través del . Si el equipo en el que se ejecuta la aplicación es compatible con el , obtendrá el mejor rendimiento mediante el uso de un dispositivo Dei.

Para crear un dispositivo, llame a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) mediante D3DDEVTYPE \_ HOLO como tipo de dispositivo.

## <a name="reference-device"></a>Dispositivo de referencia

Direct3D admite un tipo de dispositivo adicional denominado dispositivo de referencia o rasterizador de referencia. A diferencia de un dispositivo de software, el rasterizador de referencia admite todas las características de Direct3D. Este dispositivo está pensado para usarse con fines de depuración y, por tanto, solo está disponible en las máquinas en las que se ha instalado el SDK de DirectX. Dado que estas características se implementan por precisión en lugar de velocidad y se implementan en software, los resultados no son muy rápidos. El rasterizador de referencia hace uso de instrucciones especiales de CPU siempre que puede, pero no está diseñado para aplicaciones comerciales. Use el rasterizador de referencia solo con fines de demostración o prueba de características. Para crear un dispositivo de referencia, llame [**al método CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) mediante D3DDEVTYPE \_ REF como tipo de dispositivo.

## <a name="hal-vs-ref-devices"></a>Vs. Dispositivos REF frente a VSS

Los dispositivos DE REFERENCE (capa de abstracción de hardware) y los dispositivos REF (rasterizador de referencia) son los dos tipos principales de dispositivos Direct3D. el primero se basa en la compatibilidad con hardware y es muy rápido, pero es posible que no lo admita todo. mientras que el segundo no usa ninguna aceleración de hardware, por lo que es muy lento, pero se garantiza que admite todo el conjunto de características de Direct3D de la manera correcta. En general, solo tendrá que usar dispositivos DESAPER, pero si usa alguna característica avanzada que la tarjeta gráfica no admite, es posible que tenga que volver a REF.

La otra vez que quiera usar REF es si el dispositivo DE HAR genera resultados extraños, es decir, está seguro de que el código es correcto, pero el resultado no es el esperado. Se garantiza que el dispositivo REF se comporta correctamente, por lo que es posible que desee probar la aplicación en el dispositivo REF y ver si el comportamiento extraño continúa. Si no es así, significa que (a) la aplicación asume que la tarjeta gráfica admite algo que no admite, o (b) es un error del controlador. Si sigue sin funcionar con el dispositivo REF, se trata de un error de aplicación.

## <a name="hardware-vs-software-vertex-processing"></a>Procesamiento de vértices de hardware frente a software

El procesamiento de vértices de hardware frente a software solo se aplica realmente a los dispositivos DE HAED. Al insertar vértices a través de la canalización, deben transformarse (por el mundo, ver y proyectar matrices a su vez) y encenderse (por las luces integradas de D3D): esta fase de procesamiento se conoce como T&L (para Transformation & Lighting). El procesamiento de vértices de hardware significa que esto se realiza en hardware, si el hardware lo admite; y el procesamiento de vértices de software es software. La práctica general es intentar crear primero un dispositivo Hardware T&L, y si se produce un error, pruebe Mixed y, si se produce un error, pruebe software. (Si se produce un error en el software, dése por hecho y salga con un error).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 

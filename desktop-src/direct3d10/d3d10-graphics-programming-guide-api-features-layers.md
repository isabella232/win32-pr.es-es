---
description: Niveles de API (Direct3D 10)
ms.assetid: 19c81383-6ac7-49ea-98a3-bf761a32ab40
title: Niveles de API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4427083bdcaf389c4b01b590a1bc3fef7eb878b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423263"
---
# <a name="api-layers-direct3d-10"></a>Niveles de API (Direct3D 10)

El tiempo de ejecución de Direct3D 10 se construye con capas, comenzando con la funcionalidad básica en el núcleo y creando funcionalidad opcional y de ayuda para desarrolladores en capas externas.

## <a name="core-layer"></a>Nivel básico

La capa principal existe de forma predeterminada; proporcionar una asignación muy fina entre la API y el controlador de dispositivo, lo que minimiza la sobrecarga de llamadas de alta frecuencia. Como la capa principal es esencial para el rendimiento, solo realiza una validación crítica.

Las capas restantes son opcionales. Como norma general, las capas agregan funcionalidad, pero no modifican el comportamiento existente. Por ejemplo, las funciones principales tendrán los mismos valores devueltos independientemente de la capa de depuración de la que se crea una instancia, aunque se puede proporcionar una salida de depuración adicional si se crea una instancia de la capa de depuración.

Cree capas cuando se cree un dispositivo mediante una llamada a [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) y proporcione uno o varios valores de [**marca de \_ dispositivo D3D10 Create \_ Device \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) .

## <a name="debug-layer"></a>Nivel de depuración

La capa de depuración proporciona un amplio parámetro adicional y una validación de coherencia (como la validación de la vinculación del sombreador y el enlace de recursos, la validación de la coherencia de los parámetros y la notificación de descripciones La salida generada por la capa de depuración se compone de una cola de cadenas a las que se puede acceder mediante la [**interfaz ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) (vea [personalizar la salida de depuración con ID3D10InfoQueue (Direct3D 10)](d3d10-graphics-programming-guide-api-features-layers-info-queue.md)). La capa de depuración resalta los errores generados por la capa principal con advertencias.

Para crear un dispositivo que admita la capa de depuración, debe instalar el SDK de DirectX (para obtener D3D10SDKLayers.DLL) y, a continuación, especificar el \_ \_ indicador de depuración crear dispositivo de D3D10 \_ al llamar a [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice). Por supuesto, la ejecución de una aplicación con la capa de depuración será mucho más lenta. Para habilitar o deshabilitar los mensajes de depuración para las API de D3DX10, llame a [**D3DX10DebugMute**](d3dx10debugmute.md).

Cuando la capa de depuración enumera las pérdidas de memoria, genera una lista de punteros de interfaz de objetos junto con sus nombres descriptivos. El nombre descriptivo predeterminado es "sin &lt; nombre &gt; ". Puede establecer el nombre descriptivo mediante el método [**ID3D10DeviceChild:: SetPrivateData**](/windows/desktop/api/D3D10/nf-d3d10-id3d10devicechild-setprivatedata) y el GUID **WKPDID \_ D3DDebugObjectName** que se encuentra en D3Dcommon. h. Por ejemplo, para nombrar pTexture con un nombre de SDKLayer de mytexture.jpg, use el siguiente código:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



Normalmente, debe compilar estas llamadas fuera de la versión de producción.

## <a name="switch-to-reference-layer"></a>Nivel de cambio a referencia

Esta capa permite a una aplicación realizar la transición entre un dispositivo de hardware (HAL) y una referencia o dispositivo de software (REF). Para cambiar un dispositivo, primero debe crear un dispositivo que admita la capa de cambio a referencia (consulte [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) y, después, llamar a [**ID3D10SwitchToRef:: SetUseRef**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10switchtoref-setuseref).

Todos los Estados de los dispositivos, recursos y objetos se mantienen a través de esta transición del dispositivo. Sin embargo, a veces no es posible coincidir exactamente con los datos de recursos. Esto se debe al hecho de que hay información disponible para un dispositivo de hardware que no está disponible para un dispositivo de referencia.

Prácticamente todas las aplicaciones en tiempo real usan la implementación de HAL de la canalización. Cuando se cambia la canalización de un dispositivo de hardware a un dispositivo de referencia, las operaciones de representación se realizan simultáneamente en el hardware y el software. A medida que se represente el dispositivo de software, será necesario que los recursos se descarguen en la memoria del sistema. Esto puede requerir que se expulsen otros recursos almacenados en caché en la memoria del sistema para dejar espacio.

> [!Note]  
> Esta característica de nivel de cambio a referencia solo se admite en Direct3D 10 y Direct3D 10,1 y ya no se admite en Direct3D 11 y versiones posteriores.

 

## <a name="thread-safe-layer"></a>Capa de Thread-Safe

Este nivel está diseñado para permitir que las aplicaciones multiproceso tengan acceso al dispositivo desde varios subprocesos.

Una aplicación de Direct3D 10 puede controlar la sincronización de un dispositivo mediante funciones de dispositivo. Esto permite a una aplicación habilitar o deshabilitar las secciones críticas (habilitar o deshabilitar temporalmente la protección multithreading) y tomar o liberar un bloqueo de sección crítica en varios puntos de entrada de la API de Direct3D 10. La capa segura para subprocesos está habilitada de forma predeterminada. En el caso de las aplicaciones de un único subproceso, la capa segura para subprocesos no tiene ningún impacto en el rendimiento.



|                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10:<br/> A diferencia de Direct3D 9, la API de Direct3D 10 tiene como valor predeterminado la seguridad para subprocesos.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de la API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 





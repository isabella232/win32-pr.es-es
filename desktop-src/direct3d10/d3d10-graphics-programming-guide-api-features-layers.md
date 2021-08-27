---
description: Capas de API (Direct3D 10)
ms.assetid: 19c81383-6ac7-49ea-98a3-bf761a32ab40
title: Capas de API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd452032eda61c49edbf007b5ebaf0314f9054fe0b016cf07e3f4473ae3abee6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119996"
---
# <a name="api-layers-direct3d-10"></a>Capas de API (Direct3D 10)

El entorno de ejecución de Direct3D 10 se construye con capas, empezando por la funcionalidad básica en el núcleo y creando funcionalidades opcionales y de ayuda para el desarrollador en capas externas.

## <a name="core-layer"></a>Capa principal

La capa principal existe de forma predeterminada; proporcionar una asignación muy fina entre la API y el controlador de dispositivo, lo que minimiza la sobrecarga de las llamadas de alta frecuencia. Como la capa principal es esencial para el rendimiento, solo realiza una validación crítica.

Las capas restantes son opcionales. Como regla general, las capas agregan funcionalidad, pero no modifican el comportamiento existente. Por ejemplo, las funciones principales tendrán los mismos valores devueltos independientemente de la capa de depuración en la que se crea una instancia, aunque se puede proporcionar una salida de depuración adicional si se crea una instancia de la capa de depuración.

Cree capas cuando se cree un dispositivo llamando a [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) y suministrando uno o varios valores [**D3D10 \_ CREATE DEVICE \_ \_ FLAG.**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)

## <a name="debug-layer"></a>Capa de depuración

La capa de depuración proporciona una amplia validación adicional de parámetros y coherencia (como validar la vinculación del sombreador y el enlace de recursos, validar la coherencia de los parámetros y notificar descripciones de errores). La salida generada por la capa de depuración consta de una cola de cadenas a las que se puede acceder mediante la interfaz [**ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) (vea Personalizar la salida de depuración con [ID3D10InfoQueue (Direct3D 10).](d3d10-graphics-programming-guide-api-features-layers-info-queue.md) Los errores generados por la capa principal se resaltan con advertencias por la capa de depuración.

Para crear un dispositivo que admita la capa de depuración, debe instalar el SDK de DirectX (para obtener D3D10SDKLayers.DLL) y, a continuación, especificar la marca CREATE DEVICE DEBUG de D3D10 al llamar a \_ \_ \_ [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice). Por supuesto, la ejecución de una aplicación con la capa de depuración será considerablemente más lenta. Para habilitar o deshabilitar los mensajes de depuración para las API D3DX10, llame a [**D3DX10DebugMute**](d3dx10debugmute.md).

Cuando la capa de depuración enumera pérdidas de memoria, genera una lista de punteros de interfaz de objeto junto con sus nombres descriptivos. El nombre descriptivo predeterminado es &lt; "sin &gt; nombre". Puede establecer el nombre descriptivo mediante el método [**ID3D10DeviceChild::SetPrivateData**](/windows/desktop/api/D3D10/nf-d3d10-id3d10devicechild-setprivatedata) y el GUID **\_ D3DDebugObjectName de WKPDID** que se encuentra en D3Dcommon.h. Por ejemplo, para dar nombre a pTexture con un nombre SDKLayer mytexture.jpg, use el código siguiente:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



Normalmente, debe compilar estas llamadas fuera de la versión de producción.

## <a name="switch-to-reference-layer"></a>Cambiar a la capa de referencia

Esta capa permite a una aplicación realizar la transición entre un dispositivo de hardware (LOD) y un dispositivo de referencia o software (REF). Para cambiar un dispositivo, primero debe crear un dispositivo que admita la capa de cambio a referencia (vea [**D3D10CreateDevice)**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)y, a continuación, llamar a [**ID3D10SwitchToRef::SetUseRef**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10switchtoref-setuseref).

Todos los estados, recursos y objetos del dispositivo se mantienen a través de esta transición de dispositivo. Sin embargo, a veces no es posible coincidir exactamente con los datos de recursos. Esto se debe al hecho de que hay información disponible para un dispositivo de hardware que no está disponible para un dispositivo de referencia.

Prácticamente todas las aplicaciones en tiempo real usan la implementación de LA CANALIZACIÓN de la canalización. Cuando la canalización se cambia de un dispositivo de hardware a un dispositivo de referencia, las operaciones de representación se realizan simultáneamente en hardware y software. A medida que se representa el dispositivo de software, será necesario que los recursos se descarguen en la memoria del sistema. Esto puede requerir que otros recursos almacenados en caché en la memoria del sistema se expulse para hacer espacio.

> [!Note]  
> Esta característica de cambio a capa de referencia solo se admite en Direct3D 10 y Direct3D 10.1, y ya no se admite en Direct3D 11 y versiones posteriores.

 

## <a name="thread-safe-layer"></a>Thread-Safe capa

Esta capa está diseñada para permitir que las aplicaciones multiproceso accedan al dispositivo desde varios subprocesos.

Una aplicación Direct3D 10 puede controlar una sincronización de dispositivos mediante funciones de dispositivo. Esto permite a una aplicación habilitar o deshabilitar secciones críticas (habilitar o deshabilitar temporalmente la protección multithreading) y tomar o liberar un bloqueo de sección crítica en varios puntos de entrada de la API de Direct3D 10. La capa segura para subprocesos está habilitada de forma predeterminada. En el caso de las aplicaciones de un solo subproceso, la capa segura para subprocesos no tiene ningún impacto en el rendimiento.




Diferencias entre Direct3D 9 y Direct3D 10:

- A diferencia de Direct3D 9, la API de Direct3D 10 tiene como valor predeterminado la seguridad para subprocesos.



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 





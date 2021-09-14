---
title: Capas de software
description: El entorno de ejecución de Direct3D 11 se construye con capas, empezando por la funcionalidad básica en el núcleo y creando funcionalidad opcional y de ayuda para el desarrollador en capas externas. En esta sección se describe la funcionalidad de cada capa.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168530"
---
# <a name="software-layers"></a>Capas de software

El entorno de ejecución de Direct3D 11 se construye con capas, empezando por la funcionalidad básica en el núcleo y creando funcionalidad opcional y de ayuda para el desarrollador en capas externas. En esta sección se describe la funcionalidad de cada capa.

Como regla general, las capas agregan funcionalidad, pero no modifican el comportamiento existente. Por ejemplo, las funciones principales tendrán los mismos valores devueltos independientemente de la capa de depuración en la que se crea una instancia, aunque se puede proporcionar una salida de depuración adicional si se crea una instancia de la capa de depuración.

Para crear capas cuando se crea un dispositivo, llame a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) y proporcione uno o varios valores [**D3D11 \_ CREATE DEVICE \_ \_ FLAG.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)

Direct3D 11 proporciona las siguientes capas en tiempo de ejecución:

-   [Capa principal](#core-layer)
-   [Capa de depuración](#debug-layer)
-   [Temas relacionados](#related-topics)

## <a name="core-layer"></a>Capa principal

La capa principal existe de forma predeterminada; proporcionar una asignación muy fina entre la API y el controlador de dispositivo, lo que minimiza la sobrecarga de las llamadas de alta frecuencia. Como la capa principal es esencial para el rendimiento, solo realiza la validación crítica. Las capas restantes son opcionales.

## <a name="debug-layer"></a>Capa de depuración

La capa de depuración proporciona una amplia validación adicional de parámetros y coherencia (como validar la vinculación del sombreador y el enlace de recursos, validar la coherencia de los parámetros y notificar descripciones de errores).

Para crear un dispositivo que admita la capa de depuración, debe instalar el SDK de DirectX (para obtener D3D11SDKLayers.dll) y, a continuación, especificar la marca **CREATE \_ DEVICE \_ \_ DEBUG de D3D11** al llamar a la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o a la función [**D3D11CreateDeviceAndSwapChain.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) Si ejecuta la aplicación con la capa de depuración habilitada, la aplicación será considerablemente más lenta. Sin embargo, para asegurarse de que la aplicación está limpia de errores y advertencias antes de enviarla, use la capa de depuración. Para más información, consulte [Uso de la capa de depuración para depurar aplicaciones.](using-the-debug-layer-to-test-apps.md)


> [!Note]  
> Para Windows 7 con actualización de plataforma para Windows 7 (KB2670838) o Windows 8.x, para crear un dispositivo que admita la capa de depuración, instale el Kit de desarrollo de software (SDK) de Windows para Windows 8.x para obtener D3D11 \_1SDKLayers.dll.


> [!Note]  
> Por Windows 10, para crear un dispositivo que admita la capa de depuración, habilite la característica opcional "Herramientas de gráficos". Vaya al panel Configuración, en Sistema, Aplicaciones & características, Administrar características opcionales, Agregar una característica y, a continuación, busque "Herramientas de gráficos".


> [!Note]  
> Para obtener información sobre cómo depurar aplicaciones directX de forma remota, consulte Depuración remota de [aplicaciones DirectX.](/windows/desktop/direct3dtools/debugging-directx-apps-remotely)

 

Como alternativa, puede habilitar o deshabilitar la marca de depuración mediante el Panel de control [DirectX](/previous-versions//bb219725(v=vs.85)) incluido como parte del SDK de DirectX.

Cuando la capa de depuración enumera pérdidas de memoria, genera una lista de punteros de interfaz de objeto junto con sus nombres descriptivos. El nombre descriptivo predeterminado es " &lt; sin nombre &gt; ". Puede establecer el nombre descriptivo mediante el método [**ID3D11DeviceChild::SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) y el GUID **WKPDID \_ D3DDebugObjectName** que se encuentra en D3Dcommon.h. Por ejemplo, para nombrar pTexture con un nombre SDKLayer de mytexture.jpg, use el código siguiente:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



Normalmente, debe compilar estas llamadas fuera de la versión de producción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 
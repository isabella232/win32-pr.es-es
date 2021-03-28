---
title: Capas de software
description: El tiempo de ejecución de Direct3D 11 se construye con capas, comenzando con la funcionalidad básica en el núcleo y creando funcionalidad opcional y de ayuda para desarrolladores en capas externas. En esta sección se describe la funcionalidad de cada capa.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533190"
---
# <a name="software-layers"></a>Capas de software

El tiempo de ejecución de Direct3D 11 se construye con capas, comenzando con la funcionalidad básica en el núcleo y creando funcionalidad opcional y de ayuda para desarrolladores en capas externas. En esta sección se describe la funcionalidad de cada capa.

Como norma general, las capas agregan funcionalidad, pero no modifican el comportamiento existente. Por ejemplo, las funciones principales tendrán los mismos valores devueltos independientemente de la capa de depuración de la que se crea una instancia, aunque se puede proporcionar una salida de depuración adicional si se crea una instancia de la capa de depuración.

Para crear capas cuando se crea un dispositivo, llame a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) y proporcione uno o varios valores de [**\_ marca de dispositivo D3D11 Create \_ \_ Device**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) .

Direct3D 11 proporciona las siguientes capas de tiempo de ejecución:

-   [Nivel básico](#core-layer)
-   [Nivel de depuración](#debug-layer)
-   [Temas relacionados](#related-topics)

## <a name="core-layer"></a>Nivel básico

La capa principal existe de forma predeterminada; proporcionar una asignación muy fina entre la API y el controlador de dispositivo, lo que minimiza la sobrecarga de llamadas de alta frecuencia. Como la capa principal es esencial para el rendimiento, solo realiza una validación crítica. Las capas restantes son opcionales.

## <a name="debug-layer"></a>Nivel de depuración

La capa de depuración proporciona un amplio parámetro adicional y una validación de coherencia (como la validación de la vinculación del sombreador y el enlace de recursos, la validación de la coherencia de los parámetros y la notificación de descripciones

Para crear un dispositivo que admita la capa de depuración, debe instalar el SDK de DirectX (para obtener D3D11SDKLayers.dll) y, a continuación, especificar el indicador de **\_ \_ \_ depuración crear dispositivo de D3D11** al llamar a la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o a la función [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) . Si ejecuta la aplicación con la capa de depuración habilitada, la aplicación será mucho más lenta. Sin embargo, para asegurarse de que la aplicación está limpiando los errores y las advertencias antes de enviarlo, utilice la capa de depuración. Para obtener más información, vea [usar el nivel de depuración para depurar aplicaciones](using-the-debug-layer-to-test-apps.md).


> [!Note]  
> Para Windows 7 con la actualización de plataforma para Windows 7 (KB2670838) o Windows 8. x, para crear un dispositivo que admita la capa de depuración, instale el kit de desarrollo de software (SDK) de Windows para Windows 8. x para obtener D3D11 \_1SDKLayers.dll.


> [!Note]  
> En Windows 10, para crear un dispositivo que admita la capa de depuración, habilite la característica opcional "herramientas de gráficos". Vaya al panel de configuración, en sistema, aplicaciones & características, administrar características opcionales, agregar una característica y, a continuación, busque "herramientas de gráficos".


> [!Note]  
> Para obtener información sobre cómo depurar aplicaciones de DirectX de forma remota, consulte [depuración remota de aplicaciones de DirectX](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).

 

Como alternativa, puede habilitar o deshabilitar la marca de depuración mediante el [Panel de control de DirectX](/previous-versions//bb219725(v=vs.85)) incluido como parte del SDK de DirectX.

Cuando la capa de depuración enumera las pérdidas de memoria, genera una lista de punteros de interfaz de objetos junto con sus nombres descriptivos. El nombre descriptivo predeterminado es "sin &lt; nombre &gt; ". Puede establecer el nombre descriptivo mediante el método [**ID3D11DeviceChild:: SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) y el GUID **WKPDID \_ D3DDebugObjectName** que se encuentra en D3Dcommon. h. Por ejemplo, para nombrar pTexture con un nombre de SDKLayer de mytexture.jpg, use el siguiente código:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



Normalmente, debe compilar estas llamadas fuera de la versión de producción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 
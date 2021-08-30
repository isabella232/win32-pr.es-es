---
title: Migración a Direct3D 11
description: En esta sección se proporciona información para migrar a Direct3D 11 desde una versión anterior de Direct3D.
ms.assetid: 3ec8b5c2-01e6-4fbe-ada7-43898db63bbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9267005305fa001ff1c2867968048a1915c58120
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480781"
---
# <a name="migrating-to-direct3d-11"></a>Migración a Direct3D 11

En esta sección se proporciona información para migrar a Direct3D 11 desde una versión anterior de Direct3D.

-   [Direct3D 9 a Direct3D 11](#direct3d-9-to-direct3d-11)
-   [Direct3D 10 a Direct3D 11](#direct3d-10-to-direct3d-11)
    -   [Enumeraciones y define](#enumerations-and-defines)
    -   [Estructuras](#structures)
    -   [Interfaces](#interfaces)
    -   [Otras tecnologías relacionadas](#other-related-technologies)
-   [Direct3D 10.1 a Direct3D 11](#direct3d-101-to-direct3d-11)
    -   [Enumeraciones y define](#enumerations-and-defines)
    -   [Estructuras](#structures)
    -   [Interfaces](#interfaces)
-   [Nuevas características de Direct3D 11](#new-features-for-direct3d-11)
-   [Nuevas características de DirectX 11.1](#new-features-for-directx-111)
-   [Nuevas características de DirectX 11.2](#new-features-for-directx-112)
-   [Temas relacionados](#related-topics)

## <a name="direct3d-9-to-direct3d-11"></a>Direct3D 9 a Direct3D 11

La API de Direct3D 11 se basa en las mejoras de infraestructura realizadas en Direct3D 10 y 10.1. La porción de Direct3D 9 a Direct3D 11 es similar a pasar de Direct3D 9 a Direct3D 10. Estos son los principales desafíos de este esfuerzo.

-   Eliminación de todo el uso de canalización de función fija en favor de sombreadores programables creados exclusivamente en HLSL (compilados a través de D3DCompiler en lugar de D3DX9).
-   Administración de estado basada en objetos inmutables en lugar de alternancias de estado individuales.
-   Actualización para cumplir los estrictos requisitos de vinculación de diseños de entrada de búfer de vértices y firmas de sombreador.
-   Asociación de vistas de recursos de sombreador con todos los recursos de textura.
-   Asignación de todo el contenido de la imagen a un FORMATO DXGI, incluida la eliminación de todos los formatos de color de \_ 16 bits (5/5/5/1, 5/6/5, 4/4/4/4, eliminación de todos los formatos de color de 24 bits (8/8/8) y ordenación estricta del color RGB.
-   Dividir el uso de estado constante global en varios búferes constantes pequeños y actualizados de forma más eficaz.

Para obtener más información sobre cómo pasar de Direct3D 9 a Direct3D 10, vea Consideraciones [de Direct3D 9 a Direct3D 10.](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations)

## <a name="direct3d-10-to-direct3d-11"></a>Direct3D 10 a Direct3D 11

La conversión de programas escritos para usar la API de Direct3D 10 o 10.1 es un proceso directo, ya que Direct3D 11 es una extensión de la API existente. Con una única excepción secundaria (que se indica a continuación: filtrado de texto monocromático), todos los métodos y funcionalidades de Direct3D 10/10.1 están disponibles en Direct3D 11. En el esquema siguiente se describen las diferencias entre las dos API para ayudar a actualizar el código existente. Las principales diferencias aquí incluyen:

-   Las operaciones de representación (Draw, state, etc.) ya no forman parte de la interfaz Device, sino que forman parte de la nueva interfaz DeviceContext junto con los métodos de consulta de dispositivos y map/unmap de recursos.
-   Direct3D 11 incluye todas las mejoras y cambios realizados entre Direct3D 10.0 y 10.1

### <a name="enumerations-and-defines"></a>Enumeraciones y define



| Direct3D 10                            | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATO \_ DXGI                           | [**DXGI \_ FORMATO Se**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)han definido varios nuevos formatos DXGI.<br/>                                                                                                                                                                                                                                                                                                                                |
| D3D10 \_ CREATE \_ DEVICE \_ SWITCH \_ TO \_ REF | [**D3D11 \_ CREATE \_ DEVICE SWITCH TO \_ \_ \_ REF**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)La funcionalidad de cambio a referencia no es compatible con Direct3D 11.<br/>                                                                                                                                                                                                                                                                        |
| TIPO DE CONTROLADOR D3D10 \_ \_                    | [**D3D \_ DRIVER \_ TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)Tenga en cuenta que los identificadores de enumeración de [**D3D \_ DRIVER \_ TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) se han redefinido a partir de los identificadores de [**D3D10 \_ DRIVER \_ TYPE**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type). Por lo tanto, debe asegurarse de usar los identificadores de enumeración en lugar de los números literales.<br/> [**D3D \_ DRIVER \_ TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) se define en D3Dcommon.h.<br/> |
| MARCA MISC DEL RECURSO D3D10 \_ \_ \_            | [**D3D11 \_ RESOURCE \_ MISC \_ FLAG Tenga**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)en cuenta que muchas de estas marcas se han redefinido, por lo que debe asegurarse de usar identificadores de enumeración en lugar de números literales.<br/>                                                                                                                                                                                                                                |
| FILTRO D3D10 \_                          | [**D3D11 \_ FILTER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter)Tenga en cuenta que el filtrado de texto D3D10 \_ FILTER TEXT \_ \_ 1BIT se quitó de Direct3D 11. Consulte DirectWrite.<br/>                                                                                                                                                                                                                                                                            |
| CONTADOR D3D11 \_                         | [**D3D11 \_ COUNTER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_counter)Tenga en cuenta que los contadores neutrales del proveedor se quitaron para Direct3D 11, ya que rara vez se admiten.<br/>                                                                                                                                                                                                                                                                          |
| D3D10 \_ x                               | D3D11 x Muchas enumeraciones y define son \_ iguales, tienen límites mayores o tienen valores adicionales.<br/>                                                                                                                                                                                                                                                                                                               |



 

### <a name="structures"></a>Estructuras



| Direct3D 10                              | Direct3D 11                                                                                                                                                 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ENTRADA DE DECLARACIÓN DE D3D10 \_ \_ \_ SO            | [**D3D11 \_ SO \_ DECLARATION \_ ENTRY agrega**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)Stream.<br/>                                                                  |
| D3D10 \_ BLEND \_ DESC                       | [**D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)Tenga en cuenta que esta estructura ha cambiado significativamente de 10 a 10,1 para proporcionar el estado de combinación de destino de la representación.<br/> |
| D3D10 \_ BUFFER \_ DESC                      | [**D3D11 \_ BUFFER \_ DESC agrega**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)structureByteStride para su uso con recursos del sombreador de proceso<br/>                                 |
| D3D10 \_ SHADER \_ RESOURCE \_ VIEW \_ DESC      | [**D3D11 \_ SHADER \_ RESOURCE \_ VIEW \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)Tenga en cuenta que esta estructura tenía miembros de unión adicionales agregados para la versión 10.1<br/>    |
| D3D10 \_ DEPTH \_ STENCIL \_ VIEW \_ DESC        | [**D3D11 \_ DEPTH \_ STENCIL \_ VIEW \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)Tiene un nuevo miembro Flags.<br/>                                                |
| ESTADÍSTICAS DE CANALIZACIÓN DE DATOS DE CONSULTA D3D10 \_ \_ \_ \_ | [**D3D11 \_ QUERY \_ DATA \_ PIPELINE \_ STATISTICS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics)Agrega varios contadores de fase de sombreador nuevos.<br/>                  |
| D3D10 \_ x                                 | D3D11 \_ x Muchas estructuras son idénticas entre las dos API.<br/>                                                                                     |



 

### <a name="interfaces"></a>Interfaces



| Direct3D 10        | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device       | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> La interfaz del dispositivo se dividió en estas dos partes. Para la porción rápida, puede usar [**ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).<br/> Los métodos "ID3D10Device::GetTextFilterSize" y "SetTextFilerSize" ya no existen. Consulte DirectWrite.<br/> Crear \* sombreador toma un parámetro opcional adicional para [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage).<br/> \*SetShader y \* GetShader toman parámetros opcionales adicionales [**para ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)(s).<br/> [**CreateGeometryShaderWithStreamOutput toma**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) una matriz y cuenta para varios pasos de flujo de salida.<br/> El límite del parámetro NumEntries de [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) ha aumentado a D3D11 \_ SO STREAM COUNT \_ \_ \* D3D11 \_ SO OUTPUT COMPONENT COUNT en \_ \_ \_ Direct3D 11.<br/> |
| ID3D10Buffer       | [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10SwitchToRef  | [**ID3D11SwitchToRef**](/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref) La funcionalidad de cambio a referencia no se admite en Direct3D 11.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ID3D10Texture1D    | [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture2D    | [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture3D    | [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) Los métodos Map y Unmap se han movido a [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)y todos los métodos map usan [**D3D11 \_ MAPPED \_ SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) en lugar de \* \* void.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ID3D10Asynchronous | [**ID3D11Asynchronous**](/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous) Begin, End y GetData se han movido a [**ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10x            | ID3D11x Muchas interfaces son idénticas entre las dos API.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="other-related-technologies"></a>Otras tecnologías relacionadas




| Solución 10/10.1 | 11 Solución | 
|------------------|-------------|
| HLSL Complier (D3D10Compile *, D3DX10Compile)* y LAS API de reflexión de sombreador | D3DCompiler (consulte D3DCompiler.h)<blockquote>[!Note]<br />En Windows store, las API <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">D3DCompiler</a> solo se admiten para el desarrollo, no para la implementación.</blockquote><br /> | 
| Efectos 10 | <a href="https://github.com/Microsoft/FX11">Efectos 11 está</a> disponible como origen compartido en línea.<blockquote>[!Note]<br />Esta solución no es adecuada para Windows store porque requiere las <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">API D3DCompiler</a> en tiempo de ejecución (implementación).</blockquote><br /> | 
| D3DX9/D3DX10 Math | <a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a> | 
| D3DX10 | D3DX11 en el SDK de DirectX heredado <a href="https://github.com/Microsoft/DirectXTex">DirectXTex,</a> <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a>y <a href="https://github.com/Microsoft/DirectXMesh">DirectXMesh</a> ofrece alternativas a muchas tecnologías en las bibliotecas D3DX10 y D3DX11 heredadas.<br /><a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> <a href="/windows/desktop/DirectWrite/direct-write-portal">y DirectWrite</a> ofrecen compatibilidad de alta calidad para representar líneas y fuentes con estilo.<br /> | 




 

Para obtener información sobre el SDK de DirectX heredado, consulte [¿Dónde está el SDK de DirectX?](/windows/desktop/directx-sdk--august-2009-).

## <a name="direct3d-101-to-direct3d-11"></a>Direct3D 10.1 a Direct3D 11

Direct3D 10.1 es una extensión de la interfaz de Direct3D 10 y todas las características de Direct3D 10.1 están disponibles en Direct3D 11. La mayor parte de la porción de 10.1 a 11 ya se ha solucionado antes pasando de 10 a 11.

### <a name="enumerations-and-defines"></a>Enumeraciones y define



| Direct3D 10.1          | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ FEATURE \_ LEVEL1 | [**D3D \_ NIVEL \_ DE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)CARACTERÍSTICA Idéntico pero definido en D3DCommon.h más la adición de D3D FEATURE LEVEL 11 0 para hardware de clase 11 junto con \_ \_ \_ \_ D3D \_ FEATURE LEVEL \_ \_ 9 \_ 1, D3D \_ FEATURE LEVEL \_ 9 2 y \_ \_ D3D \_ FEATURE LEVEL \_ \_ 9 \_ 3 for 10level9<br/> (D3D10 \_ FEATURE \_ LEVEL \_ 9 \_ 1, D3D10 \_ FEATURE LEVEL \_ 9 2 y D3D10 FEATURE LEVEL 9 3 también se agregaron para \_ \_ \_ \_ \_ \_ 10.1 a d3d10 \_ 1.h)<br/> |



 

### <a name="structures"></a>Estructuras



| Direct3D 10.1                        | Direct3D 11                                                                                                                   |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ BLEND \_ DESC1                  | [**D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)La versión 11 es idéntica a la 10.1.<br/>                                 |
| VISTA DESC1 DEL RECURSO \_ \_ DEL SOMBREADOR \_ \_ D3D10 | [**D3D11 \_ SHADER \_ RESOURCE \_ VIEW \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)La versión 11 es idéntica a la 10.1.<br/> |



 

### <a name="interfaces"></a>Interfaces



| Direct3D 10.1             | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device1             | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> La interfaz del dispositivo se dividió en estas dos partes. Para la porción rápida, puede usar [**ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).<br/> Los métodos "ID3D10Device::GetTextFilterSize" y "SetTextFilerSize" ya no existen. Consulte DirectWrite.<br/> Crear \* sombreador toma un parámetro opcional adicional para [**ID3D11ClassLinkage.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)<br/> \*SetShader y \* GetShader toman parámetros opcionales adicionales [**para ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)(s).<br/> [**CreateGeometryShaderWithStreamOutput toma**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) una matriz y cuenta para varios pasos de flujo de salida.<br/> El límite del parámetro NumEntries de [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) ha aumentado a D3D11 \_ SO STREAM COUNT \_ \_ \* D3D11 \_ SO OUTPUT COMPONENT COUNT en \_ \_ \_ Direct3D 11.<br/> |
| ID3D10BlendState1         | [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ID3D10ShaderResourceView1 | [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="new-features-for-direct3d-11"></a>Nuevas características de Direct3D 11

Una vez que el código se actualiza para usar la API de Direct3D 11, hay numerosas [características nuevas que](direct3d-11-features.md) se deben tener en cuenta.

-   Representación multiproceso a través de listas de comandos y varios contextos
-   Implementación de algoritmos avanzados mediante el sombreador de proceso (mediante perfiles de sombreador 4.0, 4.1 o 5.0)
-   Nuevas características de hardware de 11 clases:
    -   Modelo de sombreador HLSL 5.0
    -   Vinculación dinámica del sombreador
    -   Teselación a través de sombreadores de casco y dominio
    -   Nuevos formatos de compresión de bloques: BC6H para imágenes HDR, BC7 para imágenes estándar de mayor fidelidad
-   Uso de la [tecnología 10level9](overviews-direct3d-11-devices-downlevel.md) para la representación en muchos dispositivos Shader Model 2.0 y Shader Model 3.0 a través de la API DIrect3D 11 para la compatibilidad con hardware de vídeo de nivel inferior en Windows Vista y Windows 7.
-   Aprovechar el dispositivo de representación de software WARP.

## <a name="new-features-for-directx-111"></a>Nuevas características de DirectX 11.1

Windows 8 incluye otras mejoras de gráficos de DirectX que se deben tener en cuenta al implementar el código de gráficos de DirectX, que incluyen hardware [direct3D 11.1,](direct3d-11-features.md) [DXGI 1.2,](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)modelo de controlador de pantalla [de Windows (WDDM) 1.2,](/windows-hardware/drivers/display/wddm-in-windows-8)hardware de nivel [de](overviews-direct3d-11-devices-downlevel-intro.md) característica 11.1, contextos de dispositivo Direct2D y otras mejoras.

La compatibilidad parcial con [Direct3D 11.1](direct3d-11-features.md) también está disponible en Windows 7 a través de la actualización de plataforma para [Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), que está disponible a través de la actualización de plataforma [para Windows 7](https://support.microsoft.com/kb/2670838).

## <a name="new-features-for-directx-112"></a>Nuevas características de DirectX 11.2

El Windows 8.1 incluye [Direct3D 11.2,](direct3d-11-2-features.md) [DXGI 1.3](/windows/desktop/direct3ddxgi/dxgi-1-3-improvements)y otras mejoras.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](dx-graphics-overviews.md)
</dt> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>


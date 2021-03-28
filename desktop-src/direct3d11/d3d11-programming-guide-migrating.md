---
title: Migración a Direct3D 11
description: En esta sección se proporciona información para migrar a Direct3D 11 desde una versión anterior de Direct3D.
ms.assetid: 3ec8b5c2-01e6-4fbe-ada7-43898db63bbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ade0a0d32d3f8b5c07e6653955c0c407c8fa8f
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104359470"
---
# <a name="migrating-to-direct3d-11"></a>Migración a Direct3D 11

En esta sección se proporciona información para migrar a Direct3D 11 desde una versión anterior de Direct3D.

-   [Direct3D 9 a Direct3D 11](#direct3d-9-to-direct3d-11)
-   [Direct3D 10 a Direct3D 11](#direct3d-10-to-direct3d-11)
    -   [Enumeraciones y definiciones](#enumerations-and-defines)
    -   [Estructuras](#structures)
    -   [Interfaces](#interfaces)
    -   [Otras tecnologías relacionadas](#other-related-technologies)
-   [Direct3D 10,1 a Direct3D 11](#direct3d-101-to-direct3d-11)
    -   [Enumeraciones y definiciones](#enumerations-and-defines)
    -   [Estructuras](#structures)
    -   [Interfaces](#interfaces)
-   [Nuevas características de Direct3D 11](#new-features-for-direct3d-11)
-   [Nuevas características de DirectX 11,1](#new-features-for-directx-111)
-   [Nuevas características de DirectX 11,2](#new-features-for-directx-112)
-   [Temas relacionados](#related-topics)

## <a name="direct3d-9-to-direct3d-11"></a>Direct3D 9 a Direct3D 11

La API de Direct3D 11 se basa en las mejoras de infraestructura realizadas en Direct3D 10 y 10,1. La migración de Direct3D 9 a Direct3D 11 es similar a pasar de Direct3D 9 a Direct3D 10. Estos son los principales retos de este esfuerzo.

-   Eliminación de todo el uso de la canalización de funciones fijas en favor de los sombreadores programables creados exclusivamente en HLSL (compilados mediante D3DCompiler en lugar de D3DX9).
-   Administración de Estados basada en objetos inmutables en lugar de alternar de estado individual.
-   Actualización para cumplir los requisitos estrictos de vinculación de los diseños de entrada de búfer de vértices y las firmas de sombreador.
-   Asociar vistas de recursos del sombreador con todos los recursos de textura.
-   Asignar todo el contenido de la imagen a un formato de DXGI \_ , incluida la eliminación de todos los formatos de color de 16 bits (5/5/5/1, 5/6/5, 4/4/4/4), la eliminación de todos los formatos de color de 24 bits (8/8/8) y el orden de color RGB estricto.
-   Dividir el uso de estado constante global en varios búferes de constantes pequeños y más eficaces.

Para obtener más información sobre cómo pasar de Direct3D 9 a Direct3D 10, consulte [consideraciones de Direct3D 9 a Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).

## <a name="direct3d-10-to-direct3d-11"></a>Direct3D 10 a Direct3D 11

La conversión de programas escritos para usar la API de Direct3D 10 o 10,1 es un proceso directo como Direct3D 11 es una extensión de la API existente. Con solo una excepción secundaria (que se indica a continuación-filtrado de texto monocromo), todos los métodos y la funcionalidad de Direct3D 10/10.1 están disponibles en Direct3D 11. En el siguiente esquema se describen las diferencias entre las dos API para ayudar a actualizar el código existente. Las diferencias clave aquí incluyen:

-   Las operaciones de representación (Draw, State, etc.) ya no forman parte de la interfaz del dispositivo, sino que en su lugar forman parte de la nueva interfaz DeviceContext junto con los métodos de asignación de recursos/desasignación y de consulta de dispositivos.
-   Direct3D 11 incluye todas las mejoras y los cambios realizados entre Direct3D 10,0 y 10,1

### <a name="enumerations-and-defines"></a>Enumeraciones y definiciones



| Direct3D 10                            | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| formato de DXGI \_                           | [**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)Se han definido varios formatos de DXGI nuevos.<br/>                                                                                                                                                                                                                                                                                                                                |
| D3D10 \_ Create \_ Device \_ Switch \_ to \_ ref | [**D3D11 \_ CREATE \_ Device \_ Switch \_ to \_ ref**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)la funcionalidad de cambio a referencia no es compatible con Direct3D 11.<br/>                                                                                                                                                                                                                                                                        |
| \_Tipo de controlador D3D10 \_                    | [**D3D \_ \_Tipo de controlador**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)tenga en cuenta que los identificadores de enumeración en el [**\_ \_ tipo de controlador D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) se han redefinido a partir de los identificadores en el [**\_ \_ tipo de controlador D3D10**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type). Por lo tanto, debe asegurarse de utilizar los identificadores de enumeración en lugar de números literales.<br/> [**D3D \_ El \_ tipo de controlador**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) se define en D3Dcommon. h.<br/> |
| \_Marca de recursos \_ varios \_ de D3D10            | [**D3D11 \_ \_ \_ Marcador de varios recursos**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)tenga en cuenta que muchas de estas marcas se han redefinido, por lo que debe asegurarse de usar identificadores de enumeración en lugar de números literales.<br/>                                                                                                                                                                                                                                |
| Filtro de D3D10 \_                          | [**D3D11 \_ FILTRO**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter)tenga en cuenta que el filtrado de texto D3D10 \_ filtro \_ de texto \_ 1BIT se quitó de Direct3D 11. Consulte DirectWrite.<br/>                                                                                                                                                                                                                                                                            |
| \_Contador D3D11                         | [**D3D11 \_ CONTADOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_counter)tenga en cuenta que los contadores neutros para el proveedor se han quitado para Direct3D 11, ya que rara vez se admitían.<br/>                                                                                                                                                                                                                                                                          |
| D3D10 \_ x                               | D3D11 \_ x muchas enumeraciones y definiciones son las mismas, tienen límites mayores o tienen valores adicionales.<br/>                                                                                                                                                                                                                                                                                                               |



 

### <a name="structures"></a>Estructuras



| Direct3D 10                              | Direct3D 11                                                                                                                                                 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Entrada de \_ declaración de D3D10 \_            | [**D3D11 \_ Por lo tanto, la \_ \_ entrada de declaración**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)agrega Stream.<br/>                                                                  |
| D3D10 \_ Blend \_ DESC                       | [**D3D11 \_ \_Descripción de Blend**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)tenga en cuenta que esta estructura ha cambiado significativamente de 10 a 10,1 para proporcionar el estado de mezcla de destino de representación<br/> |
| DESC. de búfer de D3D10 \_ \_                      | [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)agrega un StructureByteStride para su uso con recursos del sombreador de cálculo<br/>                                 |
| \_Vista de recursos del sombreador de D3D10 \_ \_ \_ DESC      | [**D3D11 \_ Vista de recursos del SOMBREAdor \_ \_ \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)nota esta estructura tenía miembros de Unión adicionales agregados para 10,1<br/>    |
| D3D10 \_ de \_ estarcido de profundidad \_ vista \_ DESC        | [**D3D11 \_ La \_ vista de galería de símbolos de \_ \_ profundidad**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)tiene un nuevo miembro de marcas.<br/>                                                |
| D3D10 \_ \_ estadísticas de \_ canalización de datos de consulta \_ | [**D3D11 \_ Las \_ \_ \_ estadísticas de la canalización de datos de consulta**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics)agregan varios contadores de nueva fase de sombreador.<br/>                  |
| D3D10 \_ x                                 | D3D11 \_ x muchas estructuras son idénticas entre las dos API.<br/>                                                                                     |



 

### <a name="interfaces"></a>Interfaces



| Direct3D 10        | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device       | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) y [ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> La interfaz del dispositivo se dividió en estas dos partes. Para portabilidad rápida, puede hacer uso de [**ID3D11Device:: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).<br/> Los métodos "ID3D10Device:: GetTextFilterSize" y "SetTextFilerSize" ya no existen. Consulte DirectWrite.<br/> Create \* Shader toma un parámetro opcional adicional para [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage).<br/> \*SetShader y \* GetShader toman parámetros opcionales adicionales para [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)(s).<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) toma una matriz y el recuento de varios avances de flujo de salida.<br/> El límite para el parámetro NumEntries de [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) ha aumentado a D3D11 \_ , por lo que el \_ recuento de transmisiones \_ \* D3D11 \_ para el \_ \_ \_ recuento de componentes de salida en Direct3D 11.<br/> |
| ID3D10Buffer       | [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10SwitchToRef  | [**ID3D11SwitchToRef**](/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref) No se admite la funcionalidad de cambio a referencia en Direct3D 11.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ID3D10Texture1D    | [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture2D    | [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture3D    | [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) Los métodos de asignación y desasignación se movieron a [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)y todos los métodos de asignación usan el [**\_ \_ subrecurso asignado D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) en lugar de un void \* \* .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ID3D10Asynchronous | [**ID3D11Asynchronous**](/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous) Begin, end y GetData se movieron a [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10x            | ID3D11x muchas interfaces son idénticas entre las dos API.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="other-related-technologies"></a>Otras tecnologías relacionadas



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>solución 10/10.1</th>
<th>11 solución</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>El compilador de HLSL (D3D10Compile *, D3DX10Compile*) y las API de reflexión del sombreador</td>
<td>D3DCompiler (vea D3DCompiler. h)
<blockquote>
[!Note]<br />
En el caso de las aplicaciones de la tienda Windows, las <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">API de D3DCompiler</a> solo se admiten para el desarrollo, no para la implementación.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Efectos 10</td>
<td><a href="https://github.com/Microsoft/FX11">Effects 11</a> está disponible en línea como código fuente compartido.
<blockquote>
[!Note]<br />
Esta solución no es adecuada para las aplicaciones de la tienda Windows porque requiere las <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">API de D3DCompiler</a> en tiempo de ejecución (implementación).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D3DX9/D3DX10 Math</td>
<td><a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a></td>
</tr>
<tr class="even">
<td>D3DX10</td>
<td>D3DX11 en el SDK de DirectX heredado <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a>, <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a>y <a href="https://github.com/Microsoft/DirectXMesh">DirectXMesh</a> ofrecen alternativas a muchas tecnologías de las bibliotecas heredadas de D3DX10 y D3DX11.<br/> <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> y <a href="/windows/desktop/DirectWrite/direct-write-portal">DirectWrite</a> ofrecen compatibilidad de alta calidad para representar líneas y fuentes con estilo.<br/></td>
</tr>
</tbody>
</table>



 

Para obtener información sobre el SDK de DirectX heredado, vea [¿Dónde está el SDK de DirectX?](/windows/desktop/directx-sdk--august-2009-).

## <a name="direct3d-101-to-direct3d-11"></a>Direct3D 10,1 a Direct3D 11

Direct3D 10,1 es una extensión de la interfaz de Direct3D 10 y todas las características de Direct3D 10,1 están disponibles en Direct3D 11. La mayor parte de la migración de 10,1 a 11 ya está dirigida por encima del cambio de 10 a 11.

### <a name="enumerations-and-defines"></a>Enumeraciones y definiciones



| Direct3D 10,1          | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ característica \_ Level1 | [**D3D \_ \_Nivel de característica**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)idéntico pero definido en D3DCommon. h más la adición del \_ nivel de característica de D3D \_ \_ 11 \_ 0 para un hardware de clase, junto con el nivel de característica de D3D \_ \_ \_ 9 \_ 1, el \_ \_ nivel de característica de D3D \_ 9 \_ 2 y el \_ \_ nivel de característica de D3D \_ 9 \_ 3 para 10level9<br/> (D3D10 \_ El nivel de característica 9 \_ \_ 1, el nivel de característica \_ D3D10 \_ \_ \_ 9 \_ 2 y el \_ nivel de característica D3D10 \_ \_ 9 \_ 3 también se agregaron para 10,1 a D3D10 \_ 1. h)<br/> |



 

### <a name="structures"></a>Estructuras



| Direct3D 10,1                        | Direct3D 11                                                                                                                   |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ Blend \_ DESC1                  | [**D3D11 \_ \_Descripción de Blend**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)la versión 11 es idéntica a 10,1.<br/>                                 |
| \_Vista de recursos del sombreador de D3D10 \_ \_ \_ DESC1 | [**D3D11 \_ Vista de recursos del SOMBREAdor \_ \_ \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)la versión 11 es idéntica a 10,1.<br/> |



 

### <a name="interfaces"></a>Interfaces



| Direct3D 10,1             | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device1             | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) y [ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> La interfaz del dispositivo se dividió en estas dos partes. Para portabilidad rápida, puede hacer uso de [**ID3D11Device:: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).<br/> Los métodos "ID3D10Device:: GetTextFilterSize" y "SetTextFilerSize" ya no existen. Consulte DirectWrite.<br/> Create \* Shader toma un parámetro opcional adicional para [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage).<br/> \*SetShader y \* GetShader toman parámetros opcionales adicionales para [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)(s).<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) toma una matriz y el recuento de varios avances de flujo de salida.<br/> El límite para el parámetro NumEntries de [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) ha aumentado a D3D11 \_ , por lo que el \_ recuento de transmisiones \_ \* D3D11 \_ para el \_ \_ \_ recuento de componentes de salida en Direct3D 11.<br/> |
| ID3D10BlendState1         | [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ID3D10ShaderResourceView1 | [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="new-features-for-direct3d-11"></a>Nuevas características de Direct3D 11

Una vez que el código se actualiza para usar la API de Direct3D 11, hay muchas [características nuevas](direct3d-11-features.md) que se deben tener en cuenta.

-   Representación multiproceso a través de listas de comandos y varios contextos
-   Implementación de algoritmos avanzados con el sombreador de cálculo (mediante perfiles de sombreador 4,0, 4,1 o 5,0)
-   Nuevas características de hardware de la clase 11:
    -   Modelo de sombreador HLSL 5,0
    -   Vinculación dinámica del sombreador
    -   Teselación a través de sombreadores de dominio y casco
    -   Nuevos formatos de compresión de bloque: BC6H para imágenes HDR, BC7 para imágenes estándar de mayor fidelidad
-   Uso de la [tecnología 10level9](overviews-direct3d-11-devices-downlevel.md) para la representación en muchos dispositivos del modelo de sombreador 2,0 y del modelo de sombreador 3,0 a través de la API de DIrect3D 11 para la compatibilidad con hardware de vídeo de menor calidad en Windows Vista y Windows 7.
-   Aprovechamiento del dispositivo de representación de software de dewarp.

## <a name="new-features-for-directx-111"></a>Nuevas características de DirectX 11,1

Windows 8 incluye más mejoras en los gráficos de DirectX que se deben tener en cuenta al implementar el código de gráficos de DirectX, entre los que se incluyen [Direct3D 11,1](direct3d-11-features.md), [DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements), [modelo de controladores de pantalla de Windows (WDDM) 1,2](/windows-hardware/drivers/display/wddm-in-windows-8), hardware de [nivel de característica](overviews-direct3d-11-devices-downlevel-intro.md) 11,1, contextos de dispositivo de Direct2D y otras mejoras.

La compatibilidad parcial con [Direct3D 11,1](direct3d-11-features.md) también está disponible en Windows 7, a través de la [actualización de la plataforma para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), que está disponible a través de la [actualización de la plataforma para Windows 7](https://support.microsoft.com/kb/2670838).

## <a name="new-features-for-directx-112"></a>Nuevas características de DirectX 11,2

El Windows 8.1 incluye [Direct3D 11,2](direct3d-11-2-features.md), [DXGI 1,3](/windows/desktop/direct3ddxgi/dxgi-1-3-improvements)y otras mejoras.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](dx-graphics-overviews.md)
</dt> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>


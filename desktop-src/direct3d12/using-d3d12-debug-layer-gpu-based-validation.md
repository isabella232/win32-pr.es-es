---
title: Validación basada en GPU y nivel de depuración de Direct3D 12
description: En este tema se describe cómo hacer el mejor uso de la capa de depuración de Direct3D 12. La validación basada en GPU (GBV) permite escenarios de validación en la escala de tiempo de GPU que no son posibles durante las llamadas API en la CPU.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 3160df3faf994df2abf9cf878088e84564bb5fe1
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104549163"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a>Validación basada en GPU y nivel de depuración de Direct3D 12

En este tema se describe cómo hacer el mejor uso de la capa de depuración de Direct3D 12. La validación basada en GPU (GBV) permite escenarios de validación en la escala de tiempo de GPU que no son posibles durante las llamadas API en la CPU. GBV está disponible a partir de la actualización de aniversario de herramientas de gráficos para Windows 10.

## <a name="purpose-of-gpu-based-validation"></a>Finalidad de la validación basada en GPU

La validación basada en GPU ayuda a identificar los errores siguientes:

- Uso de descriptores no inicializados o incompatibles en un sombreador.
- Uso de descriptores que hacen referencia a recursos eliminados en un sombreador.
- Validación de los Estados de los recursos promocionados y la caída del estado de los recursos.
- Indexación más allá del final del montón de descriptores en un sombreador.
- El sombreador tiene acceso a los recursos en estado incompatible.
- Uso de muestras no inicializadas o incompatibles en un sombreador.

GBV funciona mediante la creación de sombreadores revisados que tienen la validación agregada directamente al sombreador. Los sombreadores con revisión inspeccionan los argumentos raíz y los recursos a los que se tiene acceso durante la ejecución del sombreador y notifican los errores a un búfer de registro. GBV también inyecta operaciones adicionales y envía llamadas a las listas de comandos de la aplicación para validar y realizar un seguimiento de los cambios en el estado de los recursos impuesto por la lista de comandos de la escala de tiempo de GPU.

Dado que GBV requiere la capacidad de ejecutar sombreadores, las listas de comandos de copia se emulan mediante una lista de comandos de proceso. Esto podría cambiar el modo en que el hardware realiza copias, pero el resultado final no debe cambiarse. La aplicación seguirá percibiendo que se trata de listas de comandos de copia y el nivel de depuración las validará como tal.

## <a name="turning-on-gpu-based-validation"></a>Activar la validación basada en GPU

Se puede forzar el uso de GBV mediante el panel de control de DirectX (DXCPL) al forzar el nivel de depuración de Direct3D 12 y, además, forzar la validación basada en GPU (nueva pestaña en el panel de control). Una vez que se haya habilitado, GBV permanecerá habilitado hasta que se libere el dispositivo Direct3D 12. Como alternativa, GBV se puede habilitar mediante programación antes de crear el dispositivo Direct3D 12:

```cpp
void EnableShaderBasedValidation()
{
    CComPtr<ID3D12Debug> spDebugController0;
    CComPtr<ID3D12Debug1> spDebugController1;
    VERIFY(D3D12GetDebugInterface(IID_PPV_ARGS(&spDebugController0)));
    VERIFY(spDebugController0->QueryInterface(IID_PPV_ARGS(&spDebugController1)));
    spDebugController1->SetEnableGPUBasedValidation(true);
}
```

## <a name="recommended-usage"></a>Uso recomendado

En general, debe ejecutar el código con la capa de depuración habilitada la mayor parte del tiempo. Sin embargo, GBV puede ralentizar las cosas. Los desarrolladores pueden considerar la posibilidad de habilitar GBV con conjuntos de datos más pequeños (por ejemplo, demostraciones del motor o niveles de juegos pequeños con menos recursos y recursos del PSO) o durante el inicio de la aplicación temprana para reducir los problemas de rendimiento. Con contenido más grande, considere la posibilidad de activar GBV en uno o dos equipos de pruebas en un paso de prueba nocturno.

## <a name="debug-output"></a>Salida de depuración

GBV genera una salida de depuración después de que una llamada a [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) complete la ejecución en la GPU. Dado que se encuentra en la escala de tiempo de GPU, la salida de depuración puede ser asincrónica con otra validación de la escala de tiempo de la CPU. Es posible que los desarrolladores de aplicaciones deseen inyectar su propio wait-After-Execute para sincronizar la salida de depuración.

La salida de GBV identifica dónde se produjo un error en un sombreador, junto con el recuento de Draw/envío actual y las identidades de los objetos relacionados (por ejemplo, lista de comandos, cola, PSO, etc.).

## <a name="example-debug-message"></a>Ejemplo de mensaje de depuración

El siguiente mensaje de error indica que se ha tenido acceso a un recurso denominado "búfer de color principal" en un sombreador como un recurso de sombreador pero estaba en el estado de acceso desordenado cuando el sombreador se ejecutó en la GPU. También se proporciona información adicional, como la ubicación en el origen del sombreador, el nombre de la lista de comandos y el recuento de Draw (dibujar índice), y los nombres de los objetos de interfaz D3D relacionados.

```cmd
D3D12 ERROR: Incompatible resource state: Resource: 0x0000016F61A6EA80:'Main Color Buffer', 
Subresource Index: [0], 
Descriptor heap index: [0], 
Binding Type In Descriptor: SRV, 
Resource State: D3D12_RESOURCE_STATE_UNORDERED_ACCESS(0x8), 
Shader Stage: PIXEL, 
Root Parameter Index: [0], 
Draw Index: [0], 
Shader Code: E:\FileShare\MiniEngine_GitHub_160128\MiniEngine_GitHub\Core\Shaders\SharpeningUpsamplePS.hlsl(37,2-59), 
Asm Instruction Range: [0x138-0x16b], 
Asm Operand Index: [3], 
Command List: 0x0000016F6F75F740:'CommandList', SRV/UAV/CBV Descriptor Heap: 0x0000016F6F76F280:'Unnamed ID3D12DescriptorHeap Object', 
Sampler Descriptor Heap: <not set>, 
Pipeline State: 0x0000016F572C89F0:'Unnamed ID3D12PipelineState Object',  
[ EXECUTION ERROR #942: GPU_BASED_VALIDATION_INCOMPATIBLE_RESOURCE_STATE]
```

## <a name="debug-layer-apis"></a>Depurar API de capa

Para habilitar la capa de depuración, llame a [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).

Para habilitar la validación basada en GPU, llame a [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)y haga referencia a los métodos de las interfaces siguientes:

- [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

Consulte las siguientes enumeraciones y estructuras:

- [**\_Tipo de \_ parámetro de lista de comandos de depuración D3D12 \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [**\_Tipo de \_ parámetro de dispositivo de depuración D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [**\_Estado de \_ canalización de validación basada en GPU D3D12 \_ \_ \_ \_ crear \_ marcas**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [**D3D12 \_ \_ modo de \_ \_ revisión del sombreador de validación basada \_ en GPU \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [**D3D12 \_ depurar \_ \_ \_ configuración de \_ validación basada en GPU \_ \_**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [**D3D12 \_ depurar \_ \_ \_ configuración de validación basada en GPU \_ del dispositivo \_**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a>Temas relacionados

* [Descripción de la capa de depuración de Direct3D 12](understanding-the-d3d12-debug-layer.md)

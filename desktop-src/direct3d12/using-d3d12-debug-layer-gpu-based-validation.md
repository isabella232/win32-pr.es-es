---
title: Validación basada en GPU y capa de depuración de Direct3D 12
description: En este tema se describe cómo usar mejor la capa de depuración de Direct3D 12. La validación basada en GPU (GBV) permite escenarios de validación en la escala de tiempo de GPU que no son posibles durante las llamadas API en la CPU.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 63e1ebbe34bbb94fbdf52b374b10283100e3bfa432338521a9807497b236d868
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952745"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a>Validación basada en GPU y capa de depuración de Direct3D 12

En este tema se describe cómo usar mejor la capa de depuración de Direct3D 12. La validación basada en GPU (GBV) permite escenarios de validación en la escala de tiempo de GPU que no son posibles durante las llamadas API en la CPU. GBV está disponible a partir de Las herramientas de gráficos para Windows 10 de aniversario.

## <a name="purpose-of-gpu-based-validation"></a>Propósito de la validación basada en GPU

La validación basada en GPU ayuda a identificar los errores siguientes:

- Uso de descriptores no inicializados o incompatibles en un sombreador.
- Uso de descriptores que hacen referencia a recursos eliminados en un sombreador.
- Validación de estados de recursos promocionados y decadencia del estado de los recursos.
- Indexación más allá del final del montón del descriptor en un sombreador.
- Accesos de sombreador de recursos en estado incompatible.
- Uso de muestreadores no inicializados o incompatibles en un sombreador.

GBV funciona mediante la creación de sombreadores con revisión que tienen validación agregada directamente al sombreador. Los sombreadores con revisión inspeccionan los argumentos y recursos raíz a los que se ha accedido durante la ejecución del sombreador y informan de los errores a un búfer de registro. GBV también inserta operaciones adicionales y llamadas de dispatch en las listas de comandos de la aplicación para validar y realizar un seguimiento de los cambios en el estado de recursos impuestos por la lista de comandos en la escala de tiempo de GPU.

Dado que GBV requiere la capacidad de ejecutar sombreadores, las listas de comandos COPY se emulan mediante una lista de comandos COMPUTE. Esto puede cambiar el modo en que el hardware realiza copias, aunque no se debe cambiar el resultado final. La aplicación seguirá percibiendo que se trata de listas de comandos COPY y la capa de depuración las validará como tales.

## <a name="turning-on-gpu-based-validation"></a>Activación de la validación basada en GPU

Se puede forzar el uso de DirectX Panel de control (DXCPL) forzando en la capa de depuración de Direct3D 12 y, además, forzando la validación basada en GPU (nueva pestaña en el panel de control). Una vez habilitada, GBV permanecerá habilitada hasta que se lanza el dispositivo Direct3D 12. Como alternativa, GBV se puede habilitar mediante programación antes de crear el dispositivo Direct3D 12:

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

Por lo general, debe ejecutar el código con la capa de depuración habilitada la mayoría de las veces. Sin embargo, gbv puede ralentizar mucho las cosas. Los desarrolladores pueden considerar la posibilidad de habilitar GBV con conjuntos de datos más pequeños (por ejemplo, demostraciones de motor o niveles de juego pequeños con menos PSO y recursos) o durante el inicio de la aplicación para reducir los problemas de rendimiento. Con contenido mayor, considere la posibilidad de activar GBV en uno o dos equipos de prueba en un pase de prueba nocturna.

## <a name="debug-output"></a>Salida de depuración

GBV genera la salida de depuración después de que una llamada a [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) complete la ejecución en la GPU. Puesto que se encuentra en la escala de tiempo de GPU, la salida de depuración puede ser asincrónica con otra validación de escala de tiempo de CPU. Es posible que los desarrolladores de aplicaciones quieran insertar su propia espera después de la ejecución para sincronizar la salida de depuración.

La salida de GBV identifica dónde se produjo un error en un sombreador, junto con el recuento actual de draw/dispatch e identidades de objetos relacionados (por ejemplo, lista de comandos, cola, PSO, etc.).

## <a name="example-debug-message"></a>Mensaje de depuración de ejemplo

El siguiente mensaje de error indica que se ha accedido a un recurso denominado "Búfer de color principal" en un sombreador como un recurso de sombreador, pero que estaba en estado de acceso desordenado cuando el sombreador se ejecutó en la GPU. También se proporciona información adicional, como la ubicación en el origen del sombreador, el nombre de la lista de comandos y el recuento de dibujo (draw index) y los nombres de los objetos de interfaz D3D relacionados.

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

## <a name="debug-layer-apis"></a>API de nivel de depuración

Para habilitar la capa de depuración, [**llame a EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).

Para habilitar la validación basada en GPU, llame a [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)y consulte los métodos de las interfaces siguientes:

- [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

Consulte las siguientes enumeraciones y estructuras:

- [**TIPO DE PARÁMETRO D3D12 \_ DEBUG \_ COMMAND \_ LIST \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [**TIPO DE PARÁMETRO DE DISPOSITIVO \_ DE DEPURACIÓN D3D12 \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [**MARCAS CREATE DE ESTADO DE CANALIZACIÓN DE VALIDACIÓN BASADA EN GPU D3D12 \_ \_ \_ \_ \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [**MODO DE REVISIÓN DEL SOMBREADOR DE VALIDACIÓN BASADO EN GPU D3D12 \_ \_ \_ \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [**D3D12 \_ DEBUG \_ COMMAND \_ LIST \_ GPU \_ BASED \_ VALIDATION \_ SETTINGS**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [**CONFIGURACIÓN DE VALIDACIÓN BASADA EN GPU DEL DISPOSITIVO D3D12 \_ \_ \_ \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a>Temas relacionados

* [Descripción de la capa de depuración de Direct3D 12](understanding-the-d3d12-debug-layer.md)

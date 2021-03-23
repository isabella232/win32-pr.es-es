---
title: Uso de DRED para diagnosticar errores de GPU
description: El dispositivo quitó los datos extendidos (DRED) es un conjunto en evolución de características de diagnóstico diseñado para ayudarle a identificar la causa de los errores de eliminación de dispositivos inesperados.
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: bbc754239210899e804d41a294e8c9f47967fb25
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/26/2020
ms.locfileid: "104549099"
---
# <a name="use-dred-to-diagnose-gpu-faults"></a>Uso de DRED para diagnosticar errores de GPU
DRED significa que el dispositivo ha quitado los datos extendidos. DRED es un conjunto en evolución de características de diagnóstico diseñadas para ayudarle a identificar la causa de los errores de eliminación de dispositivos inesperados. En el hardware que admite las características necesarias (como se define a continuación), DRED proporciona rutas de navegación automáticas, así como informes de errores de página de GPU.

## <a name="auto-breadcrumbs"></a>Rutas de navegación automáticas
Para establecer la escena para las rutas de navegación automáticas, vamos a mencionar primero la variedad manual. En previsión de la eventualidad de una [detección y recuperación del tiempo de espera (TDR)](/windows-hardware/drivers/display/timeout-detection-and-recovery), puede usar el [método ID3D12GraphicsCommandList2:: WriteBufferImmediate](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate) para colocar las *rutas* de navegación en la secuencia de comandos de GPU, a fin de realizar un seguimiento del progreso de la GPU.

Este es un enfoque razonable si desea crear una implementación personalizada de baja sobrecarga. Sin embargo, puede que no haya parte de la versatilidad de una solución estandarizada, como las extensiones del depurador o los informes a través de [Informe de errores de Windows (WER)](/windows/desktop/wer/windows-error-reporting) (también conocido como Watson).

Por lo tanto, las rutas de navegación automáticas de DRED llaman a **WriteBufferImmediate** para colocar los contadores de progreso en la secuencia de comandos de GPU. DRED inserta una ruta de navegación después  &mdash; de cada operación de representación, lo que significa que todas las operaciones que tienen como resultado el trabajo de la GPU (por ejemplo, **dibujar**, **distribuir**, **copiar**, **resolver** y otras). Si el dispositivo se quita en medio de una carga de trabajo de GPU, el valor de ruta de navegación DRED es esencialmente una colección de las operaciones de representación que se completan antes del error.

El búfer en anillo del historial de ruta de navegación conserva hasta 64KiB operaciones en una lista de comandos determinada. Si hay más de 65536 operaciones en una lista de comandos, solo se almacenan las operaciones de último 64KiB que &mdash; sobrescriben primero las más antiguas. Sin embargo, el valor del contador de ruta de navegación sigue contado hasta `UINT_MAX` . Por lo tanto, LastOpIndex = (BreadcrumbCount-1) %65536.

DRED 1,0 estuvo disponible por primera vez en Windows 10, versión 1809 (actualización de Windows 10 de octubre de 2018) y expuso rutas de navegación integradas rudimentarias. Sin embargo, no había ninguna API para él y la única manera de habilitar Dred 1,0 era usar el **centro de comentarios** para capturar una reproducción de TDR para **aplicaciones &** el \> **rendimiento y la compatibilidad del juego** de juegos. El objetivo principal de DRED 1,0 era ayudarle a analizar los bloqueos de juegos de causa raíz a través de los comentarios de los clientes.
### <a name="caveats"></a>Advertencias
- Dado que una GPU está muy canalizada, no hay ninguna garantía de que el contador de ruta de navegación indica la operación exacta en la que se produjo un error. De hecho, en algunos dispositivos de representación diferidos basados en iconos, es posible que el contador de ruta de navegación sea una barrera de recursos completos o vista de acceso desordenado (UAV) detrás del progreso real de la GPU.
- Un controlador de pantalla puede reordenar los comandos, realizar una captura previa de la memoria del recurso correctamente antes de ejecutar un comando o vaciar la memoria caché correctamente después de la finalización de un comando. Cualquiera de estas puede producir un error de GPU. En tales casos, los contadores de ruta de navegación automática pueden ser menos útiles o engañosos.
### <a name="performance"></a>Rendimiento
Aunque las rutas de navegación automáticas están diseñadas para ser de baja sobrecarga, no son gratuitas. Las medidas empíricas muestran una pérdida de rendimiento del 2-5% en un motor de juego de gráficos AAA de Direct3D 12 típico. Por esta razón, las rutas de navegación automáticas están desactivadas de forma predeterminada.
### <a name="hardware-requirements"></a>Requisitos de hardware
Dado que los valores del contador de ruta de navegación deben conservarse después de la eliminación del dispositivo, el recurso que contiene las rutas de navegación debe existir en la memoria del sistema y debe conservarse en caso de eliminación del dispositivo. Esto significa que el controlador de pantalla debe admitir [**D3D12_FEATURE_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature). Afortunadamente, este es el caso de la mayoría de los controladores de pantalla de Direct3D 12 en Windows 10, versión 1903.
## <a name="gpu-page-fault-reporting"></a>Informe de errores de página GPU
Una característica que es nueva para DRED 1,1 es el informe de errores de página de GPU de DRED. Un error de página de GPU suele producirse en una de estas condiciones.

1. Una aplicación ejecuta erróneamente el trabajo en la GPU que hace referencia a un objeto eliminado. Esta es una de las principales razones para la eliminación inesperada de un dispositivo.
2. Una aplicación ejecuta erróneamente el trabajo en la GPU que tiene acceso a un recurso expulsado o a un icono no residente.
3. Un sombreador hace referencia a un descriptor no inicializado o obsoleto.
3. Un sombreador se indexa más allá del final de un enlace raíz.

DRED intenta resolver algunos de estos escenarios mediante la notificación de los nombres y los tipos de cualquier objeto de API existente o recientemente liberado que coincida con la dirección virtual (VA) del error de página notificado por GPU.

### <a name="caveat"></a>Cláusula
No todas las GPU admiten errores de página (aunque muchos sí). Algunas GPU responden a los errores de memoria por: Escrituras de cubo de bits; lectura de datos simulados (por ejemplo, ceros); o simplemente con el bloqueo. Desafortunadamente, en los casos en los que la GPU no se bloquea inmediatamente, la [detección y recuperación del tiempo de espera (TDR)](/windows-hardware/drivers/display/timeout-detection-and-recovery) puede producirse más adelante en la canalización, lo que dificulta la búsqueda de la causa principal.

### <a name="performance"></a>Rendimiento
El tiempo de ejecución de Direct3D 12 debe ajustar activamente una colección de objetos de API existentes y eliminados recientemente que se indexan por dirección virtual (VA). Esto aumenta la sobrecarga de la memoria del sistema e introduce una pequeña disminución del rendimiento para la creación y destrucción de objetos. Por ese motivo, este comportamiento está desactivado de forma predeterminada.

### <a name="hardware-requirements"></a>Requisitos de hardware
Una GPU que no admite errores de página puede seguir beneficiándose de la característica de rutas de navegación automáticas.

## <a name="setting-up-dred-in-code"></a>Configuración de DRED en el código
La configuración de DRED es global para el proceso y debe configurarla antes de crear un dispositivo Direct3D 12. Para ello, llame a la función [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) para recuperar un [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings).

```cpp
CComPtr<ID3D12DeviceRemovedExtendedDataSettings> pDredSettings;
VERIFY_SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&pDredSettings)));

// Turn on auto-breadcrumbs and page fault reporting.
pDredSettings->SetAutoBreadcrumbsEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
pDredSettings->SetPageFaultEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
```

> [!NOTE]
> Las modificaciones en la configuración de DRED no tienen ningún efecto en los dispositivos que ya se han creado. Sin embargo, las llamadas posteriores a [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) usan la configuración de Dred más reciente.

## <a name="accessing-dred-data-in-code"></a>Acceder a los datos de DRED en el código
Una vez detectada la eliminación del dispositivo (por ejemplo, **present** devuelve [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/com/com-error-codes-10)), use los métodos de la interfaz [**ID3D12DeviceRemovedExtendedData**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) para tener acceso a los datos de Dred para el dispositivo que se ha quitado.

Para recuperar la interfaz **ID3D12DeviceRemovedExtendedData** , llame a [QueryInterface](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) en una interfaz [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) (o derivada), pasando el identificador de interfaz (IID) de **ID3D12DeviceRemovedExtendedData**.

```cpp
void MyDeviceRemovedHandler(ID3D12Device * pDevice)
{
    CComPtr<ID3D12DeviceRemovedExtendedData> pDred;
    VERIFY_SUCCEEDED(pDevice->QueryInterface(IID_PPV_ARGS(&pDred)));
    D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT DredAutoBreadcrumbsOutput;
    D3D12_DRED_PAGE_FAULT_OUTPUT DredPageFaultOutput;
    VERIFY_SUCCEEDED(pDred->GetAutoBreadcrumbsOutput(&DredAutoBreadcrumbsOutput));
    VERIFY_SUCCEEDED(pDred->GetPageFaultAllocationOutput(&DredPageFaultOutput));
    // Custom processing of DRED data can be done here.
    // Produce telemetry...
    // Log information to console...
    // break into a debugger...
}
```

## <a name="debugger-access-to-dred"></a>Acceso del depurador a DRED
Los depuradores tienen acceso a los datos de DRED a través de **d3d12!** Exportación de datos de D3D12DeviceRemovedExtendedData.

## <a name="dred-telemetry"></a>Telemetría de DRED
La aplicación puede usar las API de DRED para controlar las características de DRED y recopilar la telemetría para ayudar a analizar los problemas. Esto le ofrece una red mucho más amplia para detectar los TDRss difíciles de reproducir.

A partir de la versión 1903 de Windows 10, todos los eventos de modo de usuario quitados se muestran en [Informe de errores de Windows (WER)](/windows/desktop/wer/windows-error-reporting), también conocido como Watson. Si una combinación determinada de aplicación, GPU y controlador de pantalla genera un número suficiente de eventos eliminados por el dispositivo, es posible que DRED se habilite temporalmente para que los clientes inicien la misma aplicación en una configuración similar.

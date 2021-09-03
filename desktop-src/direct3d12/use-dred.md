---
title: Uso de DRED para diagnosticar errores de GPU
description: Device Removed Extended Data (DRED) es un conjunto en constante evolución de características de diagnóstico diseñadas para ayudarle a identificar la causa de errores inesperados de eliminación de dispositivos.
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 795ecaf464728388c33f55655ff81d29068956ca
ms.sourcegitcommit: 9942a888f172981e276def0c6b84fb0266fcb02d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2021
ms.locfileid: "123399811"
---
# <a name="use-dred-to-diagnose-gpu-faults"></a>Uso de DRED para diagnosticar errores de GPU
DRED significa Datos extendidos quitados del dispositivo. DRED es un conjunto en constante evolución de características de diagnóstico diseñadas para ayudarle a identificar la causa de errores inesperados de eliminación de dispositivos. En el hardware que admite las características necesarias (como se define a continuación), DRED ofrece rutas de navegación automáticas, así como informes de errores de página de GPU.

## <a name="auto-breadcrumbs"></a>Rutas de navegación automáticas
Para establecer la escena de rutas de navegación automáticas, primero se mencionará la variedad manual. En previsión de la eventualidad de una detección y recuperación de tiempo de espera [(TDR),](/windows-hardware/drivers/display/timeout-detection-and-recovery)puede usar el método [ID3D12GraphicsCommandList2::WriteBufferImmediate](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate) para colocar *rutas* de navegación en el flujo de comandos de GPU, con el fin de realizar un seguimiento del progreso de la GPU.

Se trata de un enfoque razonable si desea crear una implementación personalizada de baja sobrecarga. Pero puede que falte algo de la versatilidad de una solución estandarizada, como las extensiones del depurador, o la realización de informes a través de [Informe de errores de Windows (WER) (también](/windows/desktop/wer/windows-error-reporting) conocido como Watson).

Por lo tanto, las rutas de navegación automáticas de DRED llaman a **WriteBufferImmediate** para colocar los contadores de progreso en el flujo de comandos de GPU. DRED inserta una ruta de navegación después de cada operación de representación, lo que significa que cada operación que da como resultado un trabajo de &mdash; GPU (por ejemplo, **Draw**, **Dispatch,** **Copy,** **Resolve** y otros). Si el dispositivo se quita en medio de una carga de trabajo de GPU, el valor de la ruta de navegación de DRED es básicamente una colección de las operaciones de representación que se completaron antes del error.

El búfer en anillo del historial de ruta de navegación conserva hasta 64 operacionesKiB en una lista de comandos determinada. Si hay más de 65536 operaciones en una lista de comandos, solo se almacenan las últimas operaciones de 64KiB sobrescribiendo primero las operaciones &mdash; más antiguas. Sin embargo, el valor del contador de ruta de navegación sigue contando hasta `UINT_MAX` . Por lo tanto, LastOpIndex = (BreadcrumbCount - 1) % 65536.

DRED 1.0 estaba disponible primero en Windows 10, versión 1809 (Actualización de octubre de 2018 de Windows 10) y exponía rutas de navegación automáticas rudimentarias. Sin embargo, no había NINGUNA API para ella y la única manera de habilitar DRED 1.0 era usar **Centro de opiniones** para capturar una reproducción de TDR (reproducción) para aplicaciones **de & Games** Game Performance and \> **Compatibility**. El propósito principal de DRED 1.0 era ayudar a analizar la causa principal de los bloqueos del juego a través de los comentarios de los clientes.
### <a name="caveats"></a>Advertencias
- Dado que una GPU está muy canalizada, no hay ninguna garantía de que el contador de ruta de navegación indique la operación exacta que ha producido un error. De hecho, en algunos dispositivos de representación diferida basados en mosaicos, es posible que el contador de ruta de navegación sea una barrera de recursos completos o de vista de acceso no ordenado (UAV) detrás del progreso real de la GPU.
- Un controlador para mostrar puede reordenar comandos, capturar previamente la memoria de recursos antes de ejecutar un comando o vaciar la memoria almacenada en caché después de la finalización de un comando. Cualquiera de ellos puede producir un error de GPU. En tales casos, los contadores de ruta de navegación automática pueden ser menos útiles o confusos.
### <a name="performance"></a>Rendimiento
Aunque las rutas de navegación automáticas están diseñadas para tener poca sobrecarga, no son gratuitas. Las medidas empíricas muestran una pérdida de rendimiento del 2 al 5 % en un motor de juegos gráficos típico de AAA Direct3D 12. Por este motivo, las rutas de navegación automáticas están desactivadas de forma predeterminada.
### <a name="hardware-requirements"></a>Requisitos de hardware
Dado que los valores del contador de ruta de navegación deben conservarse después de la eliminación del dispositivo, el recurso que contiene rutas de navegación debe existir en la memoria del sistema y debe conservarse en caso de eliminación del dispositivo. Esto significa que el controlador para mostrar debe admitir [**D3D12_FEATURE_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature). Afortunadamente, este es el caso de la mayoría de los controladores de pantalla de Direct3D 12 Windows 10, versión 1903.
## <a name="gpu-page-fault-reporting"></a>Informes de errores de página de GPU
Una característica nueva de DRED 1.1 es la generación de informes de errores de página de GPU dred. Un error de página de GPU se produce normalmente en una de estas condiciones.

1. Una aplicación ejecuta por error el trabajo en la GPU que hace referencia a un objeto eliminado. Esta es una de las principales razones para una eliminación inesperada del dispositivo.
2. Una aplicación ejecuta por error el trabajo en la GPU que accede a un recurso expulsado o a un icono no residentes.
3. Un sombreador hace referencia a un descriptor sin inicializar o obsoleto.
3. Un sombreador indexa más allá del final de un enlace raíz.

DRED intenta abordar algunos de estos escenarios notificando los nombres y tipos de cualquier objeto de API existente o recientemente liberada que coincida con la dirección virtual (VA) del error de página notificado por GPU.

### <a name="caveat"></a>Advertencia
No todas las GPU admiten errores de página (aunque muchos sí). Algunas GPU responden a errores de memoria mediante: escrituras de cubos de bits; leer datos simulados (por ejemplo, ceros); o simplemente ahorcando. Desafortunadamente, en los casos en los que la GPU no se bloqueo inmediatamente, puede producirse una detección y recuperación de tiempo de espera [(TDR)](/windows-hardware/drivers/display/timeout-detection-and-recovery) más adelante en la canalización, lo que dificulta aún más la localización de la causa principal.

### <a name="performance"></a>Rendimiento
El entorno de ejecución de Direct3D 12 debe mantener activamente una colección de objetos de API existentes y eliminados recientemente indexables por dirección virtual (VA). Esto aumenta la sobrecarga de memoria del sistema e introduce un pequeño impacto de rendimiento en la creación y destrucción de objetos. Por ese motivo, este comportamiento está desactivado de forma predeterminada.

### <a name="hardware-requirements"></a>Requisitos de hardware
Una GPU que no admita errores de página todavía puede beneficiarse de la característica de rutas de navegación automáticas.

## <a name="setting-up-dred-in-code"></a>Configuración de DRED en el código
La configuración de DRED es global para el proceso y debe configurarla antes de crear un dispositivo Direct3D 12. Para ello, llame a la función [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) para recuperar un [**id3D12DeviceRemovedExtendedDataSettings**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings).

```cpp
CComPtr<ID3D12DeviceRemovedExtendedDataSettings> pDredSettings;
VERIFY_SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&pDredSettings)));

// Turn on auto-breadcrumbs and page fault reporting.
pDredSettings->SetAutoBreadcrumbsEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
pDredSettings->SetPageFaultEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
```

> [!NOTE]
> Las modificaciones en la configuración de DRED no tienen ningún efecto en los dispositivos ya creados. Pero las llamadas posteriores [**a D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) usan la configuración de DRED más reciente.

## <a name="accessing-dred-data-in-code"></a>Acceso a datos DRED en el código
Después de detectar la eliminación de dispositivos (por ejemplo, **Present** devuelve DXGI_ERROR_DEVICE_REMOVED ), use los métodos de la interfaz [**ID3D12DeviceRemovedExtendedData**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) para acceder [**a**](/windows/desktop/com/com-error-codes-10)los datos DRED del dispositivo quitado.

Para recuperar la interfaz **ID3D12DeviceRemovedExtendedData,** llame a [QueryInterface](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) en una interfaz [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) (o derivada) pasando el identificador de interfaz (IID) de **ID3D12DeviceRemovedExtendedData**.

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
Los depuradores tienen acceso a los datos dred a través **de d3d12. D3D12DeviceRemovedExtendedData data** export.

## <a name="dred-telemetry"></a>Telemetría de DRED
La aplicación puede usar las API de DRED para controlar las características de DRED y recopilar telemetría para ayudar a analizar los problemas. Esto le proporciona una red mucho más amplia para detectar esos TDR difíciles de reproducir.

A partir Windows 10, versión 1903, todos los eventos quitados del dispositivo en modo de usuario se notifican [a Informe de errores de Windows (WER),](/windows/desktop/wer/windows-error-reporting)también conocido como Watson. Si una combinación determinada de aplicación, GPU y controlador de pantalla genera un número suficiente de eventos quitados del dispositivo, es posible que DRED se habilite temporalmente para los clientes que inicien la misma aplicación en una configuración similar.

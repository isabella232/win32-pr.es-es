---
title: ENUMERACIÓN DODownloadProperty
description: Especifica el identificador de las propiedades de la Optimización de distribución de descarga.
keywords:
- Enumeración DODownloadProperty, DODownloadProperty
topic_type:
- apiref
api_name:
- DODownloadProperty
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 9b9b487d01ad9a33e525e134d8d76deec8bcc9d0
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520847"
---
# <a name="dodownloadproperty-enumeration"></a>ENUMERACIÓN DODownloadProperty

La **enumeración DODownloadProperty** especifica el identificador de las propiedades de la Optimización de distribución de descarga. La interfaz **IDODownload** usa esta enumeración y la lleva a cabo un valor VARIANT, donde se encuentra el tipo de valor.

## <a name="syntax"></a>Sintaxis

```cpp
typedef enum _DODownloadProperty
{
  DODownloadProperty_Id = 0,
  DODownloadProperty_Uri,
  DODownloadProperty_ContentId,
  DODownloadProperty_DisplayName,
  DODownloadProperty_LocalPath,
  DODownloadProperty_HttpCustomHeaders,
  DODownloadProperty_CostPolicy,
  DODownloadProperty_SecurityFlags,
  DODownloadProperty_CallbackFreqPercent,
  DODownloadProperty_CallbackFreqSeconds,
  DODownloadProperty_NoProgressTimeoutSeconds,
  DODownloadProperty_ForegroundPriority,
  DODownloadProperty_BlockingMode,
  DODownloadProperty_CallbackInterface,
  DODownloadProperty_StreamInterface,
  DODownloadProperty_SecurityContext,
  DODownloadProperty_NetworkToken
  DODownloadProperty_CorrelationVector,
  DODownloadProperty_DecryptionInfo,
  DODownloadProperty_IntegrityCheckInfo,
  DODownloadProperty_IntegrityCheckMandatory,
  DODownloadProperty_TotalSizeBytes
} DODownloadProperty;
```

## <a name="constants"></a>Constantes

| Requisito | Value |
|-|-|
| DODownloadProperty_Id | Solo lectura. Use esta propiedad para obtener el identificador que identifica de forma única la descarga. El tipo VARIANT es VT_BSTR. |
| DODownloadProperty_Uri | Use esta propiedad para establecer u obtener la ruta de acceso del URI remoto del recurso que se va a descargar. Esta propiedad solo es necesaria *si DODownloadProperty_ContentId* no se proporciona. El tipo VARIANT es VT_BSTR. |
| DODownloadProperty_ContentId | Use esta propiedad para establecer u obtener el identificador de contenido único de descarga. Esta propiedad solo es necesaria *si DODownloadProperty_Uri* no se proporciona. El tipo VARIANT es VT_BSTR. |
| DODownloadProperty_DisplayName | Opcional. Use esta propiedad para establecer u obtener el nombre para mostrar de la descarga. El tipo VARIANT es VT_BSTR. |
| DODownloadProperty_LocalPath | Use esta propiedad para establecer u obtener el nombre de la ruta de acceso local para guardar el archivo de descarga. Si la ruta de acceso no existe, Optimización de distribución intentará crearla con los privilegios del autor de la llamada. Esta propiedad solo es necesaria *si DODownloadProperty_StreamInterface* no se proporcionó. El tipo VARIANT es VT_BSTR. |
| DODownloadProperty_HttpCustomHeaders | Opcional. Use esta propiedad para establecer u obtener encabezados de solicitud HTTP personalizados. Optimización de distribución estos encabezados durante las operaciones de solicitud de archivo HTTP. Los encabezados ya deben tener el formato de encabezados HTTP estándar. El tipo VARIANT es VT_BSTR. |
| DODownloadProperty_CostPolicy | Opcional. Use esta propiedad para establecer u obtener uno de los valores de enumeración **DODownloadCostPolicy.** El tipo VARIANT es VT_UI4. |
| DODownloadProperty_SecurityFlags | Solo escritura opcional. Use esta propiedad para establecer u obtener las marcas de seguridad WinHTTP estándar **(WINHTTP_OPTION_SECURITY_FLAGS**). El tipo VARIANT es VT_UI4.</br></br>Se admiten las marcas siguientes:</br>SECURITY_FLAG_IGNORE_CERT_CN_INVALID. Permite un nombre común no válido en un certificado.</br>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID. Permite una fecha de certificado no válida.</br>SECURITY_FLAG_IGNORE_UNKNOWN_CA. Permite una entidad de certificación no válida.</br>SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE. Permite establecer la identidad de un servidor con un certificado que no es de servidor.</br>WINHTTP_ENABLE_SSL_REVOCATION. Permite la revocación ssl. Si se establece esta marca, se omitirán las marcas anteriores. |
| DODownloadProperty_CallbackFreqPercent | Opcional. Use esta propiedad para establecer u obtener la frecuencia de devolución de llamada en función del porcentaje de descarga. El tipo VARIANT es VT_UI4. |
| DODownloadProperty_CallbackFreqSeconds | Opcional. Use esta propiedad para establecer u obtener la frecuencia de devolución de llamada en función del tiempo de descarga. El valor predeterminado es cada segundo. El tipo VARIANT es VT_UI4. |
| DODownloadProperty_NoProgressTimeoutSeconds | Opcional. Use esta propiedad para establecer u obtener la longitud de tiempo de espera de descarga para ningún progreso. El valor mínimo aceptado es de 60 segundos sin actividad de descarga. El tipo VARIANT es VT_UI4. |
| DODownloadProperty_ForegroundPriority | Opcional. Use esta propiedad para establecer u obtener la prioridad de descarga actual. VARIANT_TRUE valor llevará la descarga al primer plano con mayor prioridad. El valor predeterminado es prioridad en segundo plano. El tipo VARIANT es VT_BOOL. |
| DODownloadProperty_BlockingMode | Opcional. Use esta propiedad para establecer u obtener el modo de bloqueo de descarga actual. VARIANT_TRUE valor hará que **IDODownload::Start** se bloquee hasta que se complete la descarga o se haya producido un error. El valor predeterminado es el modo de no bloqueo. El tipo VARIANT es VT_BOOL. |
| DODownloadProperty_CallbackInterface | Opcional. Use esta propiedad para establecer u obtener el puntero a la interfaz **IDODownloadStatusCallback** usada para las devoluciones de llamada de descarga. El tipo VARIANT es VT_UNKNOWN. |
| DODownloadProperty_StreamInterface | Opcional. Use esta propiedad para establecer u obtener el puntero a la interfaz IStream que se usa para el tipo de descarga de flujo. El tipo VARIANT es VT_UNKNOWN. |
| DODownloadProperty_SecurityContext | Solo escritura opcional. Use esta propiedad para establecer el contexto de certificado que se usará durante las operaciones de solicitud HTTP. El valor debe constar de bytes serializados de CERT_CONTEXT. El tipo VARIANT es (VT_ARRAY \| VT_UI1). |
| DODownloadProperty_NetworkToken | Solo escritura opcional. Use esta propiedad para establecer el token de red que se usará durante las operaciones HTTP. VARIANT_TRUE valor hará que Optimización de distribución capture el token de identidad del autor de la llamada y VARIANT_FALSE borrará el token existente. El valor predeterminado es el token del usuario que ha iniciado sesión. El tipo VARIANT es VT_BOOL. |
| DODownloadProperty_CorrelationVector | Opcional. Establece un vector de correlación específico con fines de telemetría. El tipo VARIANT es VT_BSTR. |
| DODownloadProperty_DecryptionInfo | Solo escritura opcional. Establece la información de descifrado en forma de una cadena JSON. El tipo VARIANT es VT_BSTR. |
| DODownloadProperty_IntegrityCheckInfo | Solo escritura opcional. Establece la ubicación del archivo hash de fragmentos (PHF), que usa Optimización de distribución para realizar comprobaciones de integridad en tiempo de ejecución en el contenido descargado. El tipo VARIANT es VT_BSTR. |
| DODownloadProperty_IntegrityCheckMandatory | Opcional. Establece una marca booleana que indica si el uso del archivo hash de piezas (PHF) es obligatorio. Si VARIANT_TRUE, la descarga se anulará si se produce un error en la comprobación de integridad. El tipo VARIANT es VT_BOOL. |
| DODownloadProperty_TotalSizeBytes | Opcional. Especifica el tamaño total de descarga en bytes. El tipo VARIANT es VT_UI8. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | DeliveryOptimizationDownloadTypes.h |

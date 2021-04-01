---
title: Enumeración DODownloadProperty
description: Especifica el identificador de las propiedades de la operación de descarga.
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
ms.openlocfilehash: bb8ec6ad8cc55239522f953c6a81a8bf7b2b62ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150837"
---
# <a name="dodownloadproperty-enumeration"></a>Enumeración DODownloadProperty

La enumeración **DODownloadProperty** especifica el identificador de las propiedades de la operación de descarga. Esta enumeración la usa la interfaz **IDODownload** y la lleva a cabo un valor Variant, donde el tipo de valor está contenido.

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
| DODownloadProperty_Id | Solo lectura. Utilice esta propiedad para obtener el identificador que identifica de forma única la descarga. El tipo de variante es VT_BSTR. |
| DODownloadProperty_Uri | Use esta propiedad para establecer u obtener la ruta de acceso del URI remoto del recurso que se va a descargar. Esta propiedad solo es necesaria si no se proporciona *DODownloadProperty_ContentId* . El tipo de variante es VT_BSTR. |
| DODownloadProperty_ContentId | Use esta propiedad para establecer u obtener el ID. de contenido único de descarga. Esta propiedad solo es necesaria si no se proporciona *DODownloadProperty_Uri* . El tipo de variante es VT_BSTR. |
| DODownloadProperty_DisplayName | Opcional. Utilice esta propiedad para establecer u obtener el nombre para mostrar de la descarga. El tipo de variante es VT_BSTR. |
| DODownloadProperty_LocalPath | Utilice esta propiedad para establecer u obtener el nombre de la ruta de acceso local para guardar el archivo de descarga. Si la ruta de acceso no existe, intentará crearla con los privilegios del llamador. Esta propiedad solo es necesaria si no se ha proporcionado *DODownloadProperty_StreamInterface* . El tipo de variante es VT_BSTR. |
| DODownloadProperty_HttpCustomHeaders | Opcional. Utilice esta propiedad para establecer u obtener encabezados de solicitud HTTP personalizados. Incluirá estos encabezados durante las operaciones de solicitud de archivos HTTP. Los encabezados ya deben tener el formato de encabezados HTTP estándar. El tipo de variante es VT_BSTR. |
| DODownloadProperty_CostPolicy | Opcional. Utilice esta propiedad para establecer u obtener uno de los valores de enumeración **DODownloadCostPolicy** . El tipo de variante es VT_UI4. |
| DODownloadProperty_SecurityFlags | Opcional de solo escritura. Utilice esta propiedad para establecer u obtener las marcas de seguridad estándar de WinHTTP (**WINHTTP_OPTION_SECURITY_FLAGS**). El tipo de variante es VT_UI4.</br></br>Se admiten las marcas siguientes:</br>SECURITY_FLAG_IGNORE_CERT_CN_INVALID. Permite un nombre común no válido en un certificado.</br>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID. Permite una fecha de certificado no válida.</br>SECURITY_FLAG_IGNORE_UNKNOWN_CA. Permite una entidad de certificación no válida.</br>SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE. Permite establecer la identidad de un servidor con un certificado que no sea de servidor.</br>WINHTTP_ENABLE_SSL_REVOCATION. Permite la revocación de SSL. Si se establece esta marca, se omitirán las marcas anteriores. |
| DODownloadProperty_CallbackFreqPercent | Opcional. Utilice esta propiedad para establecer u obtener la frecuencia de devolución de llamada basada en el porcentaje de descarga. El tipo de variante es VT_UI4. |
| DODownloadProperty_CallbackFreqSeconds | Opcional. Utilice esta propiedad para establecer u obtener la frecuencia de devolución de llamada basada en el tiempo de descarga. El valor predeterminado es cada segundo. El tipo de variante es VT_UI4. |
| DODownloadProperty_NoProgressTimeoutSeconds | Opcional. Use esta propiedad para establecer u obtener la duración del tiempo de espera de la descarga sin progreso. El valor mínimo aceptado es de 60 segundos sin actividad de descarga. El tipo de variante es VT_UI4. |
| DODownloadProperty_ForegroundPriority | Opcional. Utilice esta propiedad para establecer u obtener la prioridad de descarga actual. VARIANT_TRUE valor devolverá la descarga al primer plano con mayor prioridad. El valor predeterminado es la prioridad de fondo. El tipo de variante es VT_BOOL. |
| DODownloadProperty_BlockingMode | Opcional. Utilice esta propiedad para establecer u obtener el modo de bloqueo de descarga actual. VARIANT_TRUE valor provocará que **IDODownload:: Start** se bloquee hasta que se complete la descarga o se produzca un error. El valor predeterminado es el modo de no bloqueo. El tipo de variante es VT_BOOL. |
| DODownloadProperty_CallbackInterface | Opcional. Utilice esta propiedad para establecer u obtener el puntero a la interfaz **IDODownloadStatusCallback** utilizada para las devoluciones de llamada de descarga. El tipo de variante es VT_UNKNOWN. |
| DODownloadProperty_StreamInterface | Opcional. Utilice esta propiedad para establecer u obtener el puntero a la interfaz IStream utilizada para el tipo de descarga de la secuencia. El tipo de variante es VT_UNKNOWN. |
| DODownloadProperty_SecurityContext | Opcional de solo escritura. Utilice esta propiedad para establecer el contexto de certificado que se utilizará durante las operaciones de solicitud HTTP. El valor debe estar compuesto de bytes serializados de CERT_CONTEXT. El tipo de variante es (VT_ARRAY \| VT_UI1). |
| DODownloadProperty_NetworkToken | Opcional de solo escritura. Utilice esta propiedad para establecer el token de red que se utilizará durante las operaciones HTTP. VARIANT_TRUE valor hará que capture el token de identidad del autor de la llamada y VARIANT_FALSE borrará el token existente. El valor predeterminado es el token del usuario que ha iniciado sesión. El tipo de variante es VT_BOOL. |
| DODownloadProperty_CorrelationVector | Opcional. Establece un vector de correlación específico para fines de telemetría. El tipo de variante es VT_BSTR. |
| DODownloadProperty_DecryptionInfo | Opcional de solo escritura. Establece la información de descifrado en forma de cadena JSON. El tipo de variante es VT_BSTR. |
| DODownloadProperty_IntegrityCheckInfo | Opcional de solo escritura. Establece la ubicación del archivo hash de elemento (PHF), que se usa para realizar comprobaciones de integridad en tiempo de ejecución en el contenido descargado. El tipo de variante es VT_BSTR. |
| DODownloadProperty_IntegrityCheckMandatory | Opcional. Establece una marca booleana que indica si el uso del archivo hash de la pieza (PHF) es obligatorio. Si VARIANT_TRUE, la descarga se anulará si se produce un error en la comprobación de integridad. El tipo de variante es VT_BOOL. |
| DODownloadProperty_TotalSizeBytes | Opcional. Especifica el tamaño total de la descarga en bytes. El tipo de variante es VT_UI8. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | DeliveryOptimizationDownloadTypes. h |

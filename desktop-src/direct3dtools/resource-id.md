---
description: Define los identificadores de recursos para los recursos de cadena compartidos.
MS-HAID: vspixengine.Resource\_Id
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración Resource_Id
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC04FDC4-CD35-4A87-8EE8-48FFA07B8FC0
api_name:
- Resource_Id
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e7d93111defb01000e32e4f5ade0c9eb09c827e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537570"
---
# <a name="span-idvspixengineresource_idspanresource_id-enumeration"></a><span id="vspixengine.resource_id"></span>\_Enumeración de ID. de recurso

Define los identificadores de recursos para los recursos de cadena compartidos. Estos se pasan al motor de captura desde el host. Se usan para mostrar cadenas en la superposición de HUD de la aplicación que se captura o para pasar valores de registro de las opciones de Visual Studio al engi de captura.

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**ID \_ ENGINEDISCONNECTED**  
No se utiliza. Identificador de recurso de la cadena que se ha usado anteriormente para indicar que se ha alcanzado PrintScreen una vez completada la sesión de captura.

<span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**RCDATA1 de IDR \_**  
No se utiliza.

<span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**contenido de IDS \_ DEFAULTEXPFILE \_**  
No se utiliza. Identificador de recurso de la cadena que se usó anteriormente para los datos XML en escenarios de captura heredados.

<span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**\_mensaje de captura de IDS \_**  
IDENTIFICADOR de recurso para la cadena "Frame capturado".

<span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**\_no se \_ \_ admite la captura de IDS**  
IDENTIFICADOR de recurso de la cadena "este programa ha indicado que no se puede usar con herramientas de Diagnóstico de gráficos".

<span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**título de captura de ID. \_ \_ no \_ admitido \_**  
IDENTIFICADOR de recurso para la cadena "funcionalidad no admitida"

<span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**\_no se \_ \_ admite la característica IDS**  
IDENTIFICADOR de recurso para la cadena "no se admite el nivel de característica del dispositivo"

<span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**ID \_ DXVERSION \_ no \_ compatible**  
IDENTIFICADOR de recurso de la cadena "DirectX version not capturable"

<span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**ID \_ DCOMP \_ no \_ compatible**  
IDENTIFICADOR de recurso de la cadena "DCOMP en uso por la aplicación, pero no compatible con este sistema operativo"

<span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**ID \_ DWRITE \_ no \_ compatible**  
IDENTIFICADOR de recurso de la cadena "DWRITE en uso por la aplicación, pero no compatible con este sistema operativo"

<span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**formato de error de ID. \_ esperado \_ \_**  
El ID. de recurso de la cadena "% s devolvió un error durante la reproducción. (HRESULT =% s) \\ r \\ n ".

<span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**mensaje de ID \_ CAPTURETOOLTIP \_**  
IDENTIFICADOR de recurso para la cadena "use la tecla Impr Pant" para capturar un fotograma. "

<span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**\_No se \_ \_ \_ \_ admiten los identificadores D2D y D10**  
El identificador de recurso de la cadena "D2D y D10 no se admite juntos en este sistema operativo"

<span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**ID. de \_ HUD \_ estadísticas**  
IDENTIFICADOR de recurso para la cadena "fotogramas capturados% d. Tiempo de marco (MS)% 0,00 f "

<span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**ID \_ ( \_ método interno)**  
IDENTIFICADOR de recurso para la cadena "método interno de DirectX"

<span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**\_marca de \_ fotogramas de captura de IDS \_**  
IDENTIFICADOR de recurso para la cadena "fotograma capturado% LD"

<span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**PIPELINESTAGE \_ INPUTASSEMBLER**  
No se utiliza.

<span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE \_ VERTEXSHADER**  
No se utiliza.

<span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE \_ HULLSHADER**  
No se utiliza.

<span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**PIPELINESTAGE \_ TESSELATOR**  
No se utiliza.

<span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE \_ DOMAINSHADER**  
No se utiliza.

<span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE \_ GEOMETRYSHADER**  
No se utiliza.

<span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE \_ STREAMOUTPUT**  
No se utiliza.

<span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**\_rasterizador PIPELINESTAGE**  
No se utiliza.

<span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE \_ u**  
No se utiliza.

<span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE \_ OUTPUTMERGER**  
No se utiliza.

<span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE \_ COMPUTESHADER**  
No se utiliza.

<span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT \_ SUPPORTEDFORMAT**  
No se utiliza.

<span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT \_ CURRENTFORMAT**  
No se utiliza.

<span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**\_encabezado BUFFEROBJECT**  
No se utiliza.

<span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**\_línea BUFFEROBJECT**  
No se utiliza.

<span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT \_ INVALIDFORMAT**  
No se utiliza.

<span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT \_ INVALIDEMPTYFORMAT**  
No se utiliza.

<span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT \_ INVALIDFORMATSIZE**  
No se utiliza.

<span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO \_ TARGETAPPLICATION**  
Texto que se muestra en la ventana Propiedades de vsglog-aplicación de destino

<span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**la \_ ruta de acceso SUMMARYINFO**  
Texto que se muestra en vsglog ventana Propiedades-path

<span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO \_ TARGETVERSION**  
Texto que se muestra en vsglog ventana Propiedades-versión de destino

<span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO \_ LastModifiedDate & gt**  
Texto que se muestra en el ventana Propiedades vsglog: fecha de última modificación

<span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**no es el \_ PROCESSID**  
Texto que se muestra en vsglog ventana Propiedades-Process ID

<span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**SUMMARYINFO \_ EXPERIMENTFILE**  
Texto que se muestra en el archivo vsglog ventana Propiedades-experimento

<span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**SUMMARYINFO \_ RUNFILE**  
Texto que se muestra en el ventana Propiedades vsglog-Run File

<span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**tamaño de SUMMARYINFO \_**  
Texto que se muestra en vsglog ventana Propiedades-size

<span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**SUMMARYINFO \_ CREATEDBYPIXVERSION**  
Texto que se muestra en el ventana Propiedades vsglog: creado por versión

<span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**SUMMARYINFO \_ SESSIONSTARTTIME**  
Texto que se muestra en la ventana Propiedades vsglog: hora de inicio de la sesión

<span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO \_ SYSTEMINFORMATION**  
Texto que se muestra en la ventana Propiedades vsglog: información del sistema

<span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**\_procesador SUMMARYINFO**  
Texto que se muestra en el procesador ventana Propiedades vsglog

<span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**\_memoria SUMMARYINFO**  
Texto que se muestra en vsglog ventana Propiedades-Memory

<span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**no \_ es SUMMARYINFO**  
Texto que se muestra en la versión vsglog ventana Propiedades-OS

<span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO \_ OSARCHITECTURE**  
Texto que se muestra en la arquitectura vsglog ventana Propiedades-OS

<span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO \_ TARGETAPPARCHITECTURE**  
Texto que se muestra en la arquitectura de la aplicación vsglog ventana Propiedades-Target

<span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**SUMMARYINFO \_ MAXHWFEATURELEVEL**  
Texto que se muestra en el nivel de características de hardware ventana Propiedades vsglog-Max

<span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**SUMMARYINFO \_ DRIVERCONCURRENTCREATES**  
Texto que se muestra en el vsglog ventana Propiedades-driver crea de forma simultánea

<span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**SUMMARYINFO \_ DRIVERCOMMANDLISTS**  
Texto que se muestra en las listas de comandos de vsglog ventana Propiedades-driver

<span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**SUMMARYINFO \_ DOUBLEPRECISIONSHADERS**  
Texto que se muestra en los sombreadores de precisión vsglog ventana Propiedades-Double

<span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**SUMMARYINFO \_ DIRECTCOMPUTECS4X**  
Texto que se muestra en vsglog ventana Propiedades-Direct Compute CS 4. x

<span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**SUMMARYINFO \_ 10BITXRHIGHCOLORFORMAT**  
Texto que se muestra en vsglog ventana Propiedades-10BITXRHIGHCOLORFORMAT

<span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**SUMMARYINFO \_ EXTENDEDCOLORFORMATSUPPORT**  
Texto que se muestra en la compatibilidad con el formato de color vsglog ventana Propiedades-Extended.

<span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**SUMMARYINFO \_ DISPLAYINFORMATION**  
Texto que se muestra en la ventana Propiedades de vsglog: Mostrar información

<span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**SUMMARYINFO \_ DISPLAYNINFORMATION**  
Texto que se muestra en el ventana Propiedades vsglog-Mostrar N información

<span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**nombre de SUMMARYINFO \_**  
Texto que se muestra en vsglog ventana Propiedades-Name

<span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**Descripción de SUMMARYINFO \_**  
Texto que se muestra en el ventana Propiedades vsglog-Description

<span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**SUMMARYINFO \_ DISPLAYMEMORY**  
Texto que se muestra en el ventana Propiedades vsglog-Mostrar memoria

<span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**SUMMARYINFO \_ DRIVERNAME**  
Texto que se muestra en el vsglog ventana Propiedades-nombre del controlador

<span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**SUMMARYINFO \_ DRIVERVERSION**  
Texto que se muestra en la versión de vsglog ventana Propiedades-driver

<span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**SUMMARYINFO \_ MODULEINFORMATION**  
Texto que se muestra en la información de vsglog ventana Propiedades-Module

<span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**SUMMARYINFO \_ DIRECT3DINFORMATION**  
Texto que se muestra en la información de ventana Propiedades vsglog-Direct3D

<span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**SUMMARYINFO \_ VSGVERSION**  
Texto que se muestra en la versión vsglog ventana Propiedades-VSG

<span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO \_ CAPTUREMACHINE**  
Texto que se muestra en la máquina vsglog ventana Propiedades-Capture

<span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO \_ PLAYBACKMACHINE**  
Texto que se muestra en la máquina de ventana Propiedades-reproducción de vsglog

<span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**\_REMOTEDATA SUMMARYINFO**  
Texto que se muestra en el ventana Propiedades de vsglog-datos remotos

<span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO \_ OtherDirect3DInformation**  
Texto que se muestra en vsglog ventana Propiedades-otra información de Direct3D

<span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO \_ SIZEGB**  
Texto que se muestra en el vsglog de tamaño ventana Propiedades GB

<span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO \_ SIZEMB**  
Texto que se muestra en vsglog ventana Propiedades-size MB

<span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO \_ bytes**  
Texto que se muestra en vsglog ventana Propiedades-size bytes

<span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO \_ MEMORYMB**  
Texto que se muestra en vsglog ventana Propiedades-Memory MB

<span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO \_ x86**  
Texto que se muestra en el ventana Propiedades vsglog-x86

<span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO \_ x64**  
Texto que se muestra en vsglog ventana Propiedades-x64

<span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO \_ true**  
Texto que se muestra en vsglog ventana Propiedades-true

<span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO \_ false**  
Texto que se muestra en el ventana Propiedades vsglog-false

<span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO \_ ARM32**  
Texto que se muestra en vsglog ventana Propiedades-ARM 32

<span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO \_ UNKNOWNCPUARCHITECTURE**  
Texto que se muestra en vsglog ventana Propiedades: arquitectura de CPU desconocida

<span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**SUMMARYINFO \_ AllDXGIFormatValues**  
Texto que se muestra en el ventana Propiedades vsglog: todos los valores de formato de DXGI

<span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**SUMMARYINFO \_ AllD3D11FormatSupportValues**  
Texto que se muestra en el formato vsglog ventana Propiedades-All D3D11 support Values

<span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**Subprocesamiento de \_ características de D3D11 SUMMARYINFO \_ \_**  
Texto que se muestra en el subproceso de la característica vsglog ventana Propiedades-D3D11 \_ \_

<span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**SUMMARYINFO \_ DriverConcurrentCreates1**  
El texto que se muestra en el vsglog ventana Propiedades-driver crea 1

<span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**SUMMARYINFO \_ DriverCommandLists1**  
Texto que se muestra en el comando vsglog ventana Propiedades-driver lists 1

<span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**Los \_ \_ dobles de características de D3D11 SUMMARYINFO \_**  
El texto que se muestra en la característica vsglog ventana Propiedades-D3D11 se \_ \_ duplica

<span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**SUMMARYINFO \_ DoublePrecisionFloatShaderOps**  
Texto que se muestra en las operaciones vsglog ventana Propiedades-Double precisión Float Shader

<span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO \_ D3D11 \_ Feature \_ D3D10 \_ X \_ Opciones de hardware \_**  
Texto que se muestra en vsglog ventana Propiedades- \_ D3D11 \_ Feature \_ D3D10 \_ X \_ Opciones de hardware

<span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO \_ ComputeShaders \_ Plus \_ RawAndStructuredBuffers \_ a través del \_ sombreador \_ 4 \_ x**  
Texto que se muestra en vsglog ventana Propiedades-ComputeShaders + RAW y Structure dBuffers a través del sombreador 4. x

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**Opciones de D3D11 de la \_ característica de D3D11 SUMMARYINFO \_ \_ \_**  
Texto que se muestra en las opciones de vsglog ventana Propiedades-D3D11 de la \_ característica \_ D3D11 \_

<span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**SUMMARYINFO \_ OutputMergerLogicOp**  
Texto que se muestra en la vsglog de la lógica de combinación de salida ventana Propiedades-Output

<span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**SUMMARYINFO \_ UAVOnlyRenderingForcedSampleCount**  
Texto que se muestra en el recuento de muestras forzada de vsglog ventana Propiedades-UAV

<span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**SUMMARYINFO \_ DiscardAPIsSeenByDriver**  
Texto que se muestra en las API vsglog ventana Propiedades-discard que ve el controlador

<span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**SUMMARYINFO \_ FlagsForUpdateAndCopySeenByDriver**  
Texto que se muestra en el vsglog ventana Propiedades: marcas de actualización y copia que ve el controlador

<span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO \_ Clearview**  
Texto que se muestra en la vista ventana Propiedades-Clear de vsglog

<span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO \_ CopyWithOverlap**  
Texto que se muestra en vsglog ventana Propiedades-Copy with superposición

<span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO \_ ConstantBufferPartialUpdate**  
Texto que se muestra en la actualización parcial del búfer vsglog ventana Propiedades-Constant

<span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO \_ ConstantBufferOffsetting**  
Texto que se muestra en el desplazamiento del búfer vsglog ventana Propiedades-Constant

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicConstantBuffer**  
Texto que se muestra en la ventana Propiedades de vsglog: no sobrescribir en el búfer de constantes dinámicas

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicBufferSRV**  
Texto que se muestra en la ventana Propiedades vsglog: no sobrescribir en el SRV de búfer dinámico

<span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO \_ MultisampleRTVWithForcedSampleCountOne**  
Texto que se muestra en vsglog ventana Propiedades-Multisample RTV con el recuento de muestras forzadas uno

<span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ SAD4ShaderInstructions**  
Texto que se muestra en las instrucciones del sombreador vsglog ventana Propiedades-SAD4

<span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ ExtendedDoublesShaderInstructions**  
Texto que se muestra en las instrucciones del sombreador de ventana Propiedades vsglog-Extended Double

<span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO \_ ExtendedResourceSharing**  
Texto que se muestra en el ventana Propiedades vsglog: uso compartido de recursos extendidos

<span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**\_Información de \_ arquitectura de características de D3D11 SUMMARYINFO \_ \_**  
Texto que se muestra en la información de \_ arquitectura de características de vsglog ventana Propiedades-D3D11 \_ \_

<span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO \_ TileBasedDeferredRenderer**  
Texto que se muestra en el representador diferido ventana Propiedades vsglog en mosaico

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**Opciones de D3D9 de la \_ característica de D3D11 SUMMARYINFO \_ \_ \_**  
Texto que se muestra en las opciones de vsglog ventana Propiedades-D3D11 de la \_ característica \_ D3D9 \_

<span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO \_ FullNonPow2TextureSupport**  
Texto que se muestra en la ventana Propiedades vsglog-Full Texture no Pow2

<span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**\_ \_ \_ \_ \_ Compatibilidad con la precisión mínima del sombreador de características de D3D11 SUMMARYINFO \_**  
Texto que se muestra en la \_ \_ \_ \_ compatibilidad con la precisión mínima del sombreador de características de vsglog ventana Propiedades-D3D11 \_

<span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO \_ PixelShaderMinPrecision**  
Texto que se muestra en la precisión mínima del sombreador de ventana Propiedades de vsglog de píxeles

<span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO \_ AllOtherShaderStagesMinPrecision**  
Texto que se muestra en el ventana Propiedades vsglog-todas las demás etapas del sombreador precisión mínima

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**D3D11, la \_ \_ característica de \_ D3D9 \_ Shadow \_ support**  
Texto que se muestra en la característica vsglog ventana Propiedades-D3D11 \_ características de \_ \_ \_ compatibilidad con instantáneas D3D9

<span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO \_ SupportsDepthAsTextureWithLessEqualComparisonFilter**  
Texto que se muestra en el ventana Propiedades vsglog: admite la profundidad como textura con un filtro de comparación menos idéntico.

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO \_ D3D11 \_ característica \_ D3D11 \_ OPTIONS1**  
Texto que se muestra en la característica vsglog ventana Propiedades-D3D11 \_ \_ D3D11 \_ OPTIONS1

<span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO \_ TiledResourcesTier**  
Texto que se muestra en el nivel de vsglog ventana Propiedades de recursos en mosaico

<span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO \_ MinMaxFiltering**  
Texto que se muestra en vsglog ventana Propiedades-Min Max Filtering

<span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO \_ ClearViewAlsoSupportsDepthOnlyFormats**  
El texto que se muestra en la vista ventana Propiedades-Clear de vsglog también admite formatos solo de profundidad

<span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO \_ MapOnDefaultBuffers**  
Texto que se muestra en el mapa de ventana Propiedades de vsglog en los búferes predeterminados

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**La \_ característica de D3D11 de la creación de instancias de D3D9 es \_ \_ \_ \_ \_ compatible.**  
Texto que se muestra en la característica vsglog ventana Propiedades-D3D11 \_ \_ D3D9 \_ \_ compatibilidad con la creación de instancias simples \_

<span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO \_ SimpleInstancingSupported0**  
Texto que se muestra en la ventana Propiedades vsglog: se admite la creación de instancias simples 0

<span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**\_ \_ \_ Compatibilidad con el marcador de características de D3D11 SUMMARYINFO \_**  
Texto que se muestra en la \_ \_ compatibilidad con el marcador de características vsglog ventana Propiedades-D3D11 \_

<span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**\_Perfil SUMMARYINFO**  
Texto que se muestra en vsglog ventana Propiedades-Profile

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO \_ D3D11 \_ característica \_ D3D9 \_ OPTIONS1**  
Texto que se muestra en la característica vsglog ventana Propiedades-D3D11 \_ \_ D3D9 \_ OPTIONS1

<span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO \_ FullNonPow2TextureSupported**  
Texto que se muestra en la vsglog ventana Propiedades-Full Texture no Pow2 compatible

<span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO \_ DepthAsTextureWithLessEqualComparisonFilterSupported**  
Texto que se muestra en vsglog ventana Propiedades-Depth como Texture con un filtro de comparación menos idéntico compatible

<span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO \_ SimpleInstancingSupported1**  
Texto que se muestra en la ventana Propiedades vsglog: se admite la creación de instancias simples 1

<span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO \_ TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**  
Texto que se muestra en el destino de representación de la esfera de vsglog ventana Propiedades-Texture con la galería de símbolos de profundidad sin cubo compatible

<span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO \_ DXGIFormat**  
Texto que se muestra en vsglog ventana Propiedades-DXGIFormat

<span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**SUMMARYINFO \_ DXGIFormat1**  
Texto que se muestra en vsglog ventana Propiedades-DXGIFormat1

<span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**\_MODULENAME SUMMARYINFO**  
Texto que se muestra en vsglog ventana Propiedades-MODULENAME

<span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**configuración de IDD \_**  
Texto que se muestra en el cuadro de diálogo configurar Firewall en el VsGraphicsRemoteEngine

<span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**\_icono de \_ encabezado \_ estático IDC**  
Texto que se muestra en el icono control de cuadro de diálogo configurar Firewall: encabezado estático

<span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**\_encabezado estático \_ IDC**  
Texto que se muestra en el encabezado de control de cuadro de diálogo configurar Firewall: estático

<span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**\_configuración de \_ FW \_ estático de IDC**  
Texto que se muestra en el control de cuadro de diálogo configurar Firewall: configuración de Firewall estática

<span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**\_icono de \_ FW \_ estático de IDC**  
Texto que se muestra en el icono de control de cuadro de diálogo configurar Firewall: estático Firewall

<span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**\_encabezado de \_ FW \_ estático de IDC**  
Texto que se muestra en el control de cuadro de diálogo configurar Firewall: encabezado de Firewall estático

<span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**\_firmware de \_ GROUPBOX \_ estático de IDC**  
Texto que se muestra en el control de cuadro de diálogo configurar Firewall: firewall de GroupBox estático

<span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**IDC, \_ comprobar las redes de \_ dominio de FW \_ \_**  
Texto que se muestra en el control de cuadro de diálogo configurar Firewall: comprobar redes de dominio de Firewall

<span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**IDC, \_ comprobación de \_ \_ redes privadas de FW \_**  
Texto que se muestra en el control de cuadro de diálogo configurar Firewall: comprobar las redes privadas del firewall

<span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**IDC, \_ comprobar las \_ \_ redes públicas de FW \_**  
Texto que se muestra en el control de cuadro de diálogo configurar Firewall: comprobar redes públicas de Firewall

<span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**botón de IDC \_ \_ configurar**  
Texto que se muestra en el control de cuadro de diálogo configurar Firewall: botón Configurar

<span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**\_cancelación de configuración de ID. \_**  
Texto que se muestra en el control de cuadro de diálogo configurar Firewall-configuración cancelar

<span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**firmware de texto de IDS \_ \_ \_ no \_ configurado**  
Texto que se muestra en el cuadro de diálogo configurar Firewall: firewall de texto no configurado

<span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**firmware de texto de ID. \_ \_ \_ configurado**  
Texto que se muestra en el cuadro de diálogo configurar Firewall: firewall de texto configurado

<span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**\_nombre de \_ regla de Firewall de IDS \_**  
Texto que se muestra en el cuadro de diálogo configurar Firewall: nombre de la regla de Firewall

<span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**Descripción de la regla de Firewall de IDS \_ \_ \_**  
Texto que se muestra en el cuadro de diálogo configurar Firewall: Descripción de la regla de Firewall

<span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**\_encabezado estático de IDS \_**  
Texto que se muestra en el encabezado del cuadro de diálogo configurar Firewall: estático

<span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**\_título de configuración de IDS \_**  
Texto que se muestra en el cuadro de diálogo configurar Firewall: título de configuración

<span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**ID. de \_ \_ encabezado de FW estático \_**  
Texto que se muestra en el cuadro de diálogo configurar Firewall: encabezado de Firewall estático

<span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**IDENTIFICADOres de \_ GROUPBOX de GROUPBOX estáticos \_ \_**  
Texto que se muestra en el cuadro de diálogo configurar Firewall: firewall de GroupBox estático

<span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**IDENTIFICADOres \_ comprobar \_ redes de dominio de FW \_ \_**  
Texto que se muestra en el cuadro de diálogo configurar Firewall: comprobar redes de dominio de Firewall

<span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**IDENTIFICADOres \_ comprobar \_ \_ redes privadas de FW \_**  
Texto que se muestra en el cuadro de diálogo configurar Firewall: comprobar redes privadas de Firewall

<span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**IDENTIFICADOres \_ comprobar \_ \_ redes públicas de FW \_**  
Texto que se muestra en el cuadro de diálogo configurar Firewall: comprobar redes públicas de Firewall

<span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**botón de identificación \_ \_ configurar**  
Texto que se muestra en el cuadro de diálogo configurar Firewall-buttom Confiture

<span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**configuración de ID. \_ \_ cancelada**  
Texto que se muestra en el cuadro de diálogo configurar Firewall-configuración cancelar

<span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**ID \_ CAPTURETOOLTIP \_ Message \_ CORESYSTEM**  
IDENTIFICADOR de recurso para la cadena "use el botón capturar de Visual Studio para capturar fotogramas".

<span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**IDENTIFICADOres y \_ \_ ninguno**  
No se utiliza.

<span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**ID. \_ et \_ SESSIONSTART**  
No se utiliza.

<span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**ID. \_ et \_ SESSIONEND**  
No se utiliza.

<span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**ID. \_ et \_ PROCESSSTART**  
No se utiliza.

<span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**ID. \_ et \_ PROCESSEND**  
No se utiliza.

<span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**ID. \_ et \_ FRAMEBEGIN**  
No se utiliza.

<span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**ID. \_ et \_ FRAMEEND**  
No se utiliza.

<span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**ID. \_ et \_ USEREVENTBEGIN**  
No se utiliza.

<span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**ID. \_ et \_ USEREVENTEND**  
No se utiliza.

<span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**ID. \_ et \_ USERMARKER**  
No se utiliza.

<span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**ID. \_ et \_ llamada**  
No se utiliza.

<span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**ID. \_ et \_ OBJECTPOPULATION**  
No se utiliza.

<span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**ID. \_ et \_ OBJECTCREATION**  
No se utiliza.

<span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**ID. \_ et \_ CALLSYNC**  
No se utiliza.

<span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**IDENTIFICADOres \_ et \_ desconocidos**  
No se utiliza.

<span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**IDENTIFICADOR no \_ desencadenar \_ ninguno**  
No se utiliza.

<span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**IDENTIFICADOR de \_ desencadenador \_ PROGRAMSTART**  
No se utiliza.

<span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**\_marco de desencadenador de IDS \_**  
No se utiliza.

<span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**\_tiempo de desencadenamiento de IDS \_**  
No se utiliza.

<span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**IDENTIFICADOR de \_ desencadenador \_ USERMARKER**  
No se utiliza.

<span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**IDENTIFICADOR de \_ desencadenador \_ BEGINUSEREVENT**  
No se utiliza.

<span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**IDENTIFICADOR de \_ desencadenador \_ ENDUSEREVENT**  
No se utiliza.

<span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**IDENTIFICADOR de \_ desencadenador \_ CAPTUREFRAME**  
No se utiliza.

<span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**IDENTIFICADOR de \_ desencadenador \_ APICAPTURE**  
No se utiliza.

<span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**ERROR de ID \_ \_ CALLDATA**  
No se utiliza.

<span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**ERROR de ID \_ \_ CREATINGLOG**  
No se utiliza.

<span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**ID \_ UNKNOWNCALL**  
No se utiliza.

<span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**nivel de característica de advertencia de ID. \_ \_ \_ \_ cambiado**  
No se utiliza.

<span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**\_frecuencia de estado de ID. \_**  

<span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID \_ deshabilitar \_ HUD**  

<span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**IDENTIFICADOR \_ deshabilitar \_ compatibilidad**  

<span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**ID \_ recopilar \_ pilas**  

<span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**IDENTIFICADOR \_ habilitar \_ detención de SDKERROR \_**  

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 




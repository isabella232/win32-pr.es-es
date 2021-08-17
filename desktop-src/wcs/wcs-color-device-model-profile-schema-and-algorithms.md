---
title: Algoritmos y esquema de perfil del modelo de dispositivo de color de WCS
description: En este tema se proporciona información sobre el esquema de perfil de modelo de dispositivo de color WCS y sus algoritmos asociados. Este tema contiene las secciones siguientes OverviewColor Device Model Profile ArchitectureThe CDMP SchemaWCS CDMP v2.0 Calibration AdditionThe CDMP Schema ElementsColorDeviceModelProfileDeviceModelNamespaceVersionVersionDocumentationCRTDevice elementLCDDevice elementProjectorDevice elementScannerDevice elementCameraDevice elementRGBPrinterDevice element HTMLPrinterDevice elementRGBVirtualDevice elementPlugInDeviceTypeRGBVirtualMeasurementTypeGammaTypeGammaOffsetGainTypeGammaOffsetGainLinearGainTypeToneResponseCurvesTypeGamutBoundarySamplesTypeFloatPairListCMYKPrinterMeasurementTypeRGBPrinterMeasurementTypeRGBCaptureMeasurementTypeOneBasedIndexRGBProjectorMeasurementTypeDisplayMeasurementTypeMeasurementConditionsTypeGeometryTypeRGBPrimariesGroupNonNegativeCMYKSampleTypeNonNegativeRGBSampleTypeNonNegativeCMYKTypeNonNegativeRGBTypeExtensionTypeNonNegativeXYZTypeXYZTypeThe  Algoritmos de línea base de CDMPCRT Device Model BaselineLCD Device Model BaselineRGB Printer Device Model BaselineRGB Virtual Device Model Baseline USB Printer Model BaselineRGB Projector Device Model BaselineICC Device Model BaselineRelated topics
ms.assetid: bbb3b50d-75fc-476d-a011-af7dcc2ac520
keywords:
- Windows Sistema de colores (WCS), perfil de modelo de dispositivo de color (CDMP)
- WCS (Windows de color), perfil de modelo de dispositivo de color (CDMP)
- administración de colores de imagen, perfil de modelo de dispositivo de color (CDMP)
- administración de colores, perfil de modelo de dispositivo de color (CDMP)
- colors,color device model profile (CDMP)
- Windows Sistema de colores (WCS), perfiles
- WCS (Windows Color System),profiles
- administración de colores de imagen, perfiles
- administración de colores, perfiles
- colors,profiles
- schemas,color device model profile (CDMP)
- algorithms,color device model profile (CDMP)
- perfil de modelo de dispositivo de color (CDMP)
- CDMP (perfil de modelo de dispositivo de color)
- Perfil de modelo de dispositivo de color WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5210da85cd320a80e6b29a59e3cb5ff37c86fd174934832404e4b52cf53bd110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118038069"
---
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a>Algoritmos y esquema de perfil del modelo de dispositivo de color de WCS

En este tema se proporciona información sobre el esquema de perfil de modelo de dispositivo de color WCS y sus algoritmos asociados.

Este tema contiene las siguientes secciones:

-   [Información general](#overview)
-   [Arquitectura del perfil de modelo de dispositivo de color](#color-device-model-profile-architecture)
-   [Esquema de CDMP](#the-cdmp-schema)
-   [Adición de calibración de WCS CDMP v2.0](#wcs-cdmp-v20-calibration-addition)
-   [Elementos de esquema de CDMP](#the-cdmp-schema-elements)
    -   [ColorDeviceModelProfile](#colordevicemodelprofile)
    -   [ColorDeviceModel](#colordevicemodelprofile)
    -   [NamespaceVersion](#namespaceversion)
    -   [Versión](#namespaceversion)
    -   [Documentación](#documentation)
    -   [CRTDevice, elemento](#crtdevice-element)
    -   [ELEMENTODEVICEDevice](#lcddevice-element)
    -   [Elemento ProjectorDevice](#projectordevice-element)
    -   [Elemento ScannerDevice](#scannerdevice-element)
    -   [Elemento CameraDevice](#cameradevice-element)
    -   [Elemento RGBPrinterDevice](#rgbprinterdevice-element)
    -   [Elemento EDITPrinterDevice](#cmykprinterdevice-element)
    -   [Elemento RGBVirtualDevice](#rgbvirtualdevice-element)
    -   [PlugInDeviceType](#plugindevicetype)
    -   [RGBVirtualMeasurementType](#rgbvirtualmeasurementtype)
    -   [GammaType](#gammatype)
    -   [GammaOffsetGainType](#gammaoffsetgaintype)
    -   [GammaOffsetGainLinearGainType](#gammaoffsetgainlineargaintype)
    -   [ToneResponseCurvesType](#toneresponsecurvestype)
    -   [GamutBoundarySamplesType](#gamutboundarysamplestype)
    -   [FloatPairList](#floatpairlist)
    -   [HOLOPrinterMeasurementType](#cmykprintermeasurementtype)
    -   [RGBPrinterMeasurementType](#rgbprintermeasurementtype)
    -   [RGBCaptureMeasurementType](#rgbcapturemeasurementtype)
    -   [OneBasedIndex](#onebasedindex)
    -   [RGBProjectorMeasurementType](#rgbprojectormeasurementtype)
    -   [DisplayMeasurementType](#displaymeasurementtype)
    -   [MeasurementConditionsType](#measurementconditionstype)
    -   [GeometryType](#geometrytype)
    -   [RGBPrimariesGroup](#rgbprimariesgroup)
    -   [NonNegativeSAMPLESampleType](#nonnegativecmyksampletype)
    -   [NonNegativeRGBSampleType](#nonnegativergbsampletype)
    -   [NonNegativeTYPEType](#nonnegativecmyktype)
    -   [NonNegativeRGBType](#nonnegativergbtype)
    -   [ExtensionType](#extensiontype)
    -   [NonNegativeXYZType](#nonnegativexyztype)
    -   [XYZType](#nonnegativexyztype)
-   [Algoritmos de línea base de CDMP](#the-cdmp-baseline-algorithms)
    -   [Línea base del modelo de dispositivo CRT](#crt-device-model-baseline)
    -   [Línea de base del modelo de dispositivos DE LÍNEA DE TELÉFONO](#lcd-device-model-baseline)
    -   [Línea base del modelo de dispositivo de impresora RGB](#rgb-printer-device-model-baseline)
    -   [Línea base del modelo de dispositivo virtual RGB](#rgb-virtual-device-model-baseline)
    -   [Línea base del modelo de dispositivo de impresora PRINTER](#cmyk-printer-device-model-baseline)
    -   [Línea base del modelo de dispositivo del proyector RGB](#rgb-projector-device-model-baseline)
    -   [Línea de base del modelo de dispositivo DE LAC](#icc-device-model-baseline)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Este esquema se usa para especificar el contenido de un perfil de modelo de dispositivo de color (CDMP). A continuación se describen los algoritmos de línea base asociados.

El esquema de perfil de modelo de dispositivo básico (DMP) consta de los datos de medición de muestreo.

El componente de muestreo del esquema XML de DMP proporciona compatibilidad con los destinos de medición de color básicos, centrándose en destinos estándar comunes y destinos optimizados para los modelos de dispositivo de línea de base.

Además, el perfil de dispositivo proporciona información específica sobre el modelo de dispositivo de destino y proporciona una directiva que el modelo de dispositivo de reserva de línea base puede usar si el modelo de destino no está disponible. Las instancias de perfil pueden incluir extensiones privadas mediante mecanismos de extensión XML estándar.

## <a name="color-device-model-profile-architecture"></a>Arquitectura del perfil de modelo de dispositivo de color

![Diagrama que muestra la información que forma un perfil de modelo de dispositivo.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a>Esquema de CDMP


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="RGBType">
    <xs:attribute name="R" type="xs:float" use="required"/>
    <xs:attribute name="G" type="xs:float" use="required"/>
    <xs:attribute name="B" type="xs:float" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeRGBType">
    <xs:attribute name="R" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="G" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="B" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeCMYKType">
    <xs:attribute name="C" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="M" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="K" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeRGBSampleType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:NonNegativeRGBType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeCMYKSampleType">
    <xs:sequence>
      <xs:element name="CMYK" type="cdm:NonNegativeCMYKType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:group name="RGBPrimariesGroup">
    <xs:sequence>
      <xs:element name="WhitePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="RedPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="GreenPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BluePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BlackPrimary" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
  </xs:group> 
  
  <xs:complexType name="MeasurementConditionsType">
    <xs:annotation>
      <xs:documentation>
      Optional measurement conditions. 
       
      We only support CIEXYZ for measurement color space in this version. 
      If the white point value from the measurement conditions is not available, 
      the default processing will use
        - "D50" for printer and scanners
        - "D65" for camera and displays.          
      </xs:documentation>
    </xs:annotation>
    <xs:sequence>
      <xs:element name="ColorSpace" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="CIEXYZ"/>
          </xs:restriction>
        </xs:simpleType>    
      </xs:element>
      <xs:choice minOccurs="0">
        <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
        <xs:element name="WhitePointName">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="D50"/>
              <xs:enumeration value="D65"/>
              <xs:enumeration value="A"/>
              <xs:enumeration value="F2"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:choice>
      <xs:element name="Geometry" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="0/45"/>
            <xs:enumeration value="0/diffuse"/>
            <xs:enumeration value="diffuse/0"/>
            <xs:enumeration value="direct"/>
          </xs:restriction>
        </xs:simpleType>   
      </xs:element>
      <xs:element name="ApertureSize" type="xs:int" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="DisplayMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="GrayRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="RedRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="GreenRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="BlueRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBProjectorMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:simpleType name="OneBasedIndex">
    <xs:restriction base="xs:int">
      <xs:minInclusive value="1"/>
    </xs:restriction>
  </xs:simpleType>
    
  <xs:complexType name="RGBCaptureMeasurementType">
    <xs:sequence>
      <xs:element name="PrimaryIndex">
        <xs:complexType>
          <xs:all>
            <xs:element name="White" type="cdm:OneBasedIndex"/>
            <xs:element name="Black" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Red" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Green" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Blue" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Cyan" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Magenta" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Yellow" type="cdm:OneBasedIndex" minOccurs="0"/>
          </xs:all>
        </xs:complexType>
      </xs:element>
      <xs:element name="NeutralIndices">
        <xs:simpleType>
          <xs:list itemType="cdm:OneBasedIndex"/>
        </xs:simpleType>
      </xs:element>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:complexType name="CMYKPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeCMYKSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="GammaType">
    <xs:attribute name="value" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="GammaOffsetGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="GammaOffsetGainLinearGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="LinearGain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="cdm:FloatList"/>
      <xs:element name="Output" type="cdm:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="cdm:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="0" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="GamutBoundarySamplesType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:RGBType" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="RGBVirtualMeasurementType">
    <xs:sequence>
      <xs:element name="MaxColorantUsed" type="xs:float"/>
      <xs:element name="MinColorantUsed" type="xs:float"/>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:choice>
        <xs:element name="Gamma" type="cdm:GammaType"/>
        <xs:element name="GammaOffsetGain" type="cdm:GammaOffsetGainType"/>
        <xs:element name="GammaOffsetGainLinearGain" type="cdm:GammaOffsetGainLinearGainType"/>
        <xs:element name="HDRToneResponseCurves" type="cdm:HDRToneResponseCurvesType"/>
      </xs:choice>
      <xs:element name="GamutBoundarySamples" type="cdm:GamutBoundarySamplesType" minOccurs="0"/>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="MeasurementConditions" type="cdm:MeasurementConditionsType" minOccurs="0"/>
        <xs:element name="SelfLuminous" type="xs:boolean" />
        <xs:element name="MaxColorant" type="xs:float"/>
        <xs:element name="MinColorant" type="xs:float"/>
        <xs:choice>
          <xs:element name="CRTDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="LCDDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBProjectorDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBProjectorMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="ScannerDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CameraDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CMYKPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:CMYKPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBVirtualDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBVirtualMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
        </xs:choice>
        <xs:element name="PlugInDevice" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>

```



## <a name="wcs-cdmp-v20-calibration-addition"></a>Adición de calibración de WCS CDMP v2.0

El **elemento ColorDeviceModel** del esquema CDMP se ha actualizado en Windows 7 para incluir el nuevo elemento de calibración. A continuación se muestra el cambio en el esquema de CDMP.


```C++
  ...
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        ...
        <xs:element name="PlugInDevice" minOccurs="0">
             ...
        </xs:element>
        <xs:element name="Calibration" type="cal:Calibration" minOccurs="0"/>
        ...
      <xs:sequence>
    ...
    <xs:complexType>
  ...
```



## <a name="the-cdmp-schema-elements"></a>Elementos de esquema de CDMP

> [!Note]  
> Las principales son ejemplos principales de rojo, verde, azul, negro y blanco. Una rampa principal es una rampa tonal desde la mínima luminosidad hasta el valor principal completo. El número máximo de entradas en una rampa de tono es 4096.

 

> [!Note]  
> Las DMP deben tener datos de medida.

 

### <a name="colordevicemodelprofile"></a>ColorDeviceModelProfile

Este elemento es de tipo ColorDeviceModel.

**Condiciones de validación:** Cada sub element se valida por su propio tipo.

### <a name="colordevicemodel"></a>ColorDeviceModel

Este elemento es una secuencia de los siguientes sub-elementos

1.  Cadena ProfileName,
2.  cadena de descripción opcional,
3.  cadena de autor opcional,
4.  MeasurementConditions MeasurementConditionsType opcional,
5.  Self-Luminous booleano,
6.  MaxColorant float,
7.  MinColorant float,
8.  Elección de elementos
    1.  CRTDevice,
    2.  DEVICEDevice,
    3.  RGBProjectorDevice,
    4.  ScannerDevice,
    5.  CameraDevice,
    6.  RGBPrinterDevice,
    7.  EDITPrinterDevice,
    8.  RGBVirtualDevice,
9.  PlugInDevice,
10. ExtensionType opcional

**Condiciones de validación:** Cada sub element se valida por su propio tipo. Los sub elements de cadena tienen un máximo de 10 000 caracteres. El sub element MaxColorant debe ser mayor o igual que cero (0) y mayor que el sub element MinColorant. MinColorant puede ser negativo.

### <a name="namespaceversion"></a>NamespaceVersion

xmlns:cdm=" http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

targetNamespace=" http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

### <a name="version"></a>Versión

Versión = "1.0" con Windows Vista.

**Condiciones de validación:** Cualquier valor de &gt; versión 0.1 o =2.0 es válido para admitir cambios no importantes &lt; en el formato.

### <a name="documentation"></a>Documentación

Esquema del perfil del modelo de dispositivo.

Copyright (C) Microsoft. All rights reserved.

### <a name="crtdevice-element"></a>CRTDevice, elemento

Este elemento es una secuencia de sub-elementos de MeasurementData DisplayMeasurementType.

**Condiciones de validación:** Cada sub element se valida por su propio tipo.

### <a name="lcddevice-element"></a>ELEMENTODEVICEDevice

Este elemento es una secuencia de sub-elementos de MeasurementData DisplayMeasurementType.

**Condiciones de validación:** Cada sub element se valida por su propio tipo.

### <a name="projectordevice-element"></a>Elemento ProjectorDevice

Este elemento es una secuencia de sub elementos de measurementData RGBProjectorMeasurementType.

**Condiciones de validación:** Cada sub element se valida por su propio tipo.

### <a name="scannerdevice-element"></a>Elemento ScannerDevice

Este elemento es una secuencia de sub-elementos de measurementData RGBCaptureMeasurementType

**Condiciones de validación:** Cada sub element se valida por su propio tipo.

### <a name="cameradevice-element"></a>Elemento CameraDevice

Este elemento es una secuencia de sub-elementos de measurementData RGBCaptureMeasurementType

**Condiciones de validación:** Cada sub element se valida por su propio tipo.

### <a name="rgbprinterdevice-element"></a>Elemento RGBPrinterDevice

Este elemento es una secuencia de sub elementos de measurementData RGBPrinterMeasurementType.

**Condiciones de validación:** Cada sub element se valida por su propio tipo.

### <a name="cmykprinterdevice-element"></a>Elemento EDITPrinterDevice

Este elemento es una secuencia de sub-elementos de measurementData OPENPrinterMeasurementType.

**Condiciones de validación:** Cada sub element se valida por su propio tipo.

### <a name="rgbvirtualdevice-element"></a>Elemento RGBVirtualDevice

Este elemento es una secuencia de sub-elementos de RGBVirtualMeasurementDataType.

**Condiciones de validación:** Cada sub element se valida por su propio tipo.

### <a name="plugindevicetype"></a>PlugInDeviceType

Este elemento es una secuencia de UN GUIDType y cualquier subdominio.

**Condiciones de validación:** El GUID se usa para coincidir con el GUID del archivo DLL del complemento dm. Hay un máximo de 100 000 elementos secundarios personalizados.

### <a name="rgbvirtualmeasurementtype"></a>RGBVirtualMeasurementType

Este elemento es una secuencia que consta de

1.  Grupo RGBPrimariesGroup
2.  Una opción de
3.  -   Gamma
    -   GammaOffsetGain
    -   GammaOffsetGainLinearGam
    -   Elementos ToneResponseCurves

4.  Opcional GamutBoundarySamples GamutBoundarySamplesType
5.  TimeStamp dateTime

**Condiciones de validación:** Cada sub element de estos tipos tiene sus propias condiciones de validación.

### <a name="gammatype"></a>GammaType

Este elemento es un tipo complejo que consta del atributo .

-   Gamma NonNegativeFloatType

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="gammaoffsetgaintype"></a>GammaOffsetGainType

Este elemento es un tipo complejo que consta de los atributos

-   Gamma NonNegativeFloatType
-   Offset NonNegativeFloatType
-   Gain NonNegativeFloatType

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="gammaoffsetgainlineargaintype"></a>GammaOffsetGainLinearGainType

Este elemento es un tipo complejo que consta de los atributos

-   Gamma NonNegativeFloatType
-   Offset NonNegativeFloatType
-   Gain NonNegativeFloatType
-   LinearGain NonNegativeFloatType
-   TransitionPoint NonNegativeFloatType.

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="toneresponsecurvestype"></a>ToneResponseCurvesType

Este elemento es una secuencia de

1.  RedTRC FloatPairList
2.  GreenTRC FloatPairList
3.  BlueTRC FloatPairList

El elemento también tiene un atributo TRCLength de tipo unsignedint.

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="gamutboundarysamplestype"></a>GamutBoundarySamplesType

Este elemento es una secuencia de RGBTypes.

**Condiciones de validación:** Actualmente, las ocurrencias máximas sin enlazar se deben enlazar en función de los comentarios del sector.

### <a name="floatpairlist"></a>FloatPairList

Este elemento es un tipo simple de lista de pares de flotantes.

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="cmykprintermeasurementtype"></a>HOLOPrinterMeasurementType

Este elemento es un

1. secuencia del elemento ColorCube que consta de una secuencia de Sample NonNegativeSAMPLESampleType

2. Atributo DateTime de TimeStamp.

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="rgbprintermeasurementtype"></a>RGBPrinterMeasurementType

Este elemento es un

1. secuencia del elemento ColorCube que consta de una secuencia de Sample NonNegativeRGBSampleType

2. Atributo DateTime de TimeStamp.

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="rgbcapturemeasurementtype"></a>RGBCaptureMeasurementType

Este elemento es una secuencia de

1.  PrimaryIndex complexType de
2.  1.  White OneBasedIndex
    2.  OneBasedIndex negro opcional
    3.  Red OneBasedIndex opcional
    4.  OneBasedIndex verde opcional
    5.  OneBasedIndex azul opcional
    6.  Opcional OneBasedIndex
    7.  Optional Magenta OneBasedIndex
    8.  OneBasedIndex amarillo opcional

3.  NeutralIndices de líneas de OneBasedIndex
4.  Secuencia ColorSamples de Sample NonNegativeRGBSampleType

El elemento también tiene un atributo DateTime de TimeStamp.

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="onebasedindex"></a>OneBasedIndex

Este elemento es un tipo simple de restricción base unsigned int con valor minInclusive = "1".

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="rgbprojectormeasurementtype"></a>RGBProjectorMeasurementType

Este elemento es una secuencia de

1.  Grupo RGBPrimariesGroup
2.  Elemento ColorSamples que consta de una secuencia de Sample NonNegativeRGBSampleType

El elemento también tiene un atributo DateTime de TimeStamp.

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="displaymeasurementtype"></a>DisplayMeasurementType

Este elemento es una secuencia de

1.  group RGBPrimariesGroup
2.  GrayRamp de secuencia de Sample NonNegativeRGBType
3.  RedRamp de secuencia de Sample NonNegativeRGBType
4.  GreenRamp de secuencia de Sample NonNegativeRGBType
5.  BlueRamp de secuencia de Sample NonNegativeRGBType

El elemento DisplayMeasurementType también tiene un atributo DateTime de TimeStamp.

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="measurementconditionstype"></a>MeasurementConditionsType

MeasurementConditionsType es una secuencia de elementos secundarios que contiene:

1.  Valor de enumeración de cadenas restringidas de ColorSpace de "CIEXYZ"
2.  opción opcional de enumeración de cadenas NonNegativeXYZType o WhitePointName de los valores D50, D65, A o F2
3.  Geometry GeometryType
4.  ApertureSize entero en milímetros

Los valores predeterminados son:

1.  Impresoras RGB y RGB:
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  ApertureSize de 10 mm
2.  Escáneres:
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  ApertureSize de 10 mm
3.  Pantallas y dispositivo virtual RGB:
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  0/45 GeometryType
    4.  ApertureSize de 10 mm
4.  Cámaras:
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  GeometryType directo
    4.  ApertureSize de 10 mm

**Condiciones de validación:** La validación de cada sub element viene determinada por las condiciones de validación para esos subconsúmenes. Si falta algún sub element, se usa el valor predeterminado específico del tipo de modelo de dispositivo.

### <a name="geometrytype"></a>GeometryType

String

Valores de enumeración:

-   "0/45"
-   "0/difuso"
-   "difuso/0"
-   "Direct"

**Condiciones de validación:** Cualquier valor excepto los valores de enumberation enumerados no es válido. Esta información no cambiará el comportamiento del procesamiento de línea de base.

### <a name="rgbprimariesgroup"></a>RGBPrimariesGroup

Este elemento es una secuencia de

1.  WhitePrimary NonNegativeXYZType
2.  RedPrimary NonNegativeXYZType
3.  GreenPrimary NonNegativeXYZType
4.  BluePrimary NonNegativeXYZTYpe
5.  BlackPrimary NonNegativeXYZType

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="nonnegativecmyksampletype"></a>NonNegativeSAMPLESampleType

Este elemento es una secuencia de

1.  HOLO NonNegativeTYPEType
2.  CIEXYZ NonNegativeXYZType

El elemento también tiene una cadena de etiqueta de atributo opcional.

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="nonnegativergbsampletype"></a>NonNegativeRGBSampleType

Este elemento es una secuencia de

1.  RGB NonNegativeRGBType
2.  CIEXYZ NonNegativeXYZType

El elemento también tiene una cadena de etiqueta de atributo opcional.

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="nonnegativecmyktype"></a>NonNegativeTYPEType

Este elemento que consta de atributos

1.  C float
2.  M float
3.  Y float
4.  K float

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="nonnegativergbtype"></a>NonNegativeRGBType

Este elemento que consta de atributos

1.  R float
2.  G float
3.  B float

**Condiciones de validación:** Que se determine a partir de los comentarios del sector.

### <a name="extensiontype"></a>ExtensionType

El elemento ExtensionType es una secuencia de cualquier tipo de sub element y se usa para la información de propiedad de aplicaciones que no son de Microsoft.

**Condiciones de validación:** Este elemento es opcional. Puede haber un máximo de 1000 elementos secundarios de extensión.

### <a name="nonnegativexyztype"></a>NonNegativeXYZType

El elemento NonNegativeXYZType se compone de nonNegativeFloatType de tres elementos de punto flotante IEEE de precisión sencilla denominados "X", "Y" y "Z". Estos valores se limitan a los valores de medida de los perfiles de DMP. Estas medidas pueden ser valores reflectantes absolutos (no relativos) de CIEXYZ 1931 o valores directos (no relativos) de CIEXYZ 1931 directos (transmisivos) en candelas por medidor de unidades cuadradas.

**Condiciones de validación:** Solo los valores reales son válidos y los valores de medida de CIEXYZ negativos no son válidos. Dado que se trata de valores absolutos, los valores pueden ser mayores que 1,0f. Un límite razonable para cualquier "X", "Y" o "Z". Value se establece arbitrariamente en 10000.0f.

### <a name="xyztype"></a>XYZType

El elemento XYZType se compone de tres valores de punto flotante IEEE de precisión sencilla: "X", "Y" y "Z".

## <a name="the-cdmp-baseline-algorithms"></a>Algoritmos de línea base de CDMP

### <a name="crt-device-model-baseline"></a>Línea base del modelo de dispositivo CRT

Para comprender este modelo, debe tener en cuenta tanto el proceso de caracterización como el modelado de dispositivos. En el proceso de caracterización, las medidas XYZ se realizan primero en los colores obtenidos rellenando el búfer de visualización de un dispositivo de visualización crt. Los valores de ejemplo siguientes generarán buenos datos para el modelo de dispositivo CRT de línea de base:

Rojo: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = 0

Azul: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutros: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255

También se pueden usar incrementos distintos de 15 e incrementos no lineales. Cada rampa roja, verde, azul y neutra debe contener al menos tres muestras, pero se recomienda proporcionar más muestras. Debe proporcionar ejemplos para rojo puro, verde, azul, negro y blanco. Los ejemplos no tienen que estar espaciados uniformemente.

El proceso de creación de la matriz tmulmulus consta de dos pasos. En primer lugar, calcule el valor XYZ de punto negro o el desancha. Este paso se basa en gran medida en el trabajo de Berns 3 con una función objetivo ligeramente modificada \[ \] para la optimización no lineal. En segundo lugar, calcule la matriz tmulmulus en función del resultado del paso uno y también de un cálculo de promedio en todas las medidas por canal, no solo en la del recuento digital máximo.

Cada uno de estos pasos contiene procedimientos detallados. El punto de partida son las rampas (17 pasos en nuestro ejemplo) para cada uno de los canales R, G y B. Cuando las medidas XYZ se trazan en el *xy-plane* de la cazticidad, se muestra una situación típica en la figura 1. El primer paso consiste en resolver un problema de optimización no lineal para encontrar el punto negro de "mejor ajuste" que minimice el desfasado a medida que atraviesa los canales R, G y B. En función de Berns \[ \] 3, buscamos ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z <sub>K</sub>* ) que minimiza la siguiente función objetivo:

![Muestra la función de objetivo donde Sr, Sg y Sb son el conjunto de puntos de datos en los canales R, G y B.](images/cdmp-formula1.png)

donde *S <sub>R,</sub>**S <sub>G</sub>* y *S <sub>B</sub>* son el conjunto de puntos de datos correspondientes a los puntos de los canales R, G y B. Para cualquier conjunto *S*, defina:

![Muestra una fórmula para definir cualquier conjunto S.](images/cdmp-formula2.png)

En el anterior, S es la cardinalidad de \|  \| *S,* es decir, el número de puntos del conjunto S . ![ Muestra una fórmula para la simplicidad de un punto.](images/cdmp-formula3.png) es las coordenadas de siticidad del punto ![ Muestra un formaula para un punto.](images/cdmp-formula4.png) , por lo que muestra una fórmula para el promedio o el centro de masa. , es el promedio, o centro de masa, de todos los puntos del conjunto S en el plano de ![ ](images/cdmp-formula5.png) siticidad.  Por lo ![ tanto, muestra una fórmula para la suma de un segundo momento de puntos.](images/cdmp-formula6.png) es la suma de los segundos momentos de los puntos sobre el centro de masa y es una medida de cómo se reparten los puntos sobre él. Por último, ![ muestra una fórmula para la medida total de la propagación de tres clústeres de puntos.](images/cdmp-formula7.png) es una medida total de cómo se reparten los tres clústeres de puntos sobre sus respectivos centros de masa.

En el cálculo de ![ Muestra una fórmula de f(X,Y,Z; Xk, Yk, Zk).](images/cdmp-formula8.png) , si muestra una fórmula para X. , se omite el cálculo y la cardinalidad de ![ S se ajusta en ](images/cdmp-formula9.png) consecuencia. 

A pesar de la complejidad aparente de la función objective, es una suma de los cuadrados de muchas funciones diferenciables en *X <sub>K</sub>*,*Y <sub>K</sub>Z <sub>K</sub>* (17 puntos 2 *xy* -components 3 canales = 102, en el ejemplo) y, por lo tanto, es amenable a las técnicas estándar de mínimos cuadrados no lineales, como el algoritmo Levenberg-Marquardt, que es el algoritmo utilizado en WCS. Tenga en cuenta que la función objetivo anterior es diferente de la sugerida en Berns 3 en que esta última función mide la varianza de las distancias desde el centro de la masa, de modo que la varianza es cero cuando los puntos son equidistantes desde el centro de la masa, aunque se puedan propagar bastante \[ \] al respecto. En el ejemplo, la dispersión de puntos se conciba directamente mediante los segundos momentos.

Al igual que con cualquier algoritmo iterativo para el problema de mínimos cuadrados no lineales, Levenberg-Marquardt requiere una suposición inicial. Hay dos candidatos obvios. Uno es (0, 0, 0); el otro es el punto negro medido. Para la CTE, el punto negro medido se usa primero como suposición inicial. Si se supera un máximo de 100 iteraciones sin alcanzar un umbral de una distancia media de 0,001 de cada punto desde su centro de masa (que corresponde a un valor de umbral de (0,001) 17 3 = 0,000051 para la función objetivo), se realiza otra ronda de iteraciones con la suposición inicial de (0, 0, 0). La estimación resultante del punto negro es XYZ en comparación con la mejor estimación de la ronda anterior de iteraciones (con el punto negro medido como suposición inicial). Use la estimación que proporciona el valor más pequeño para la función de objetivo. La elección de 100 iteraciones y la distancia de error de 0,001 se seleccionaron empíricamente. En versiones futuras, podría ser razonable parametrizar la distancia de error.

El resultado del paso uno es el punto negro estimado *(X <sub>K</sub>*,*Y <sub>K,</sub>**Z <sub>K</sub>* ). El paso dos consiste en determinar la matriz tmulmulus al calcular el promedio de la simplicidad de los puntos de los tres clústeres obtenidos en el paso uno. En el caso de los CRT, esto se realiza principalmente para minimizar los efectos de los errores de medición. Los puntos usados para promediar la tosca deben ser los mismos que se usaron en la optimización en el paso uno. En otras palabras, si el primer punto (recuento digital 15, en el ejemplo) de cada rampa se descarta en el paso de optimización, se debe hacer lo mismo en el promedio. Si ![ muestra fórmulas de promedio de tronía para coordenadas en los canales rojo y verde.](images/cdmp-formula10.png) , y ![ Muestra una fórmula de la tosca promedio para coordenadas en el canal azul.](images/cdmp-formula11.png) son las coordenadas de tonificación medias de los canales rojo, verde y azul; a continuación, el procedimiento siguiente determina la matriz tmulus. En primer lugar, resuelva el sistema lineal 3?3:

![Muestra la primera parte del procedimiento para resolver un sistema lineal 3?3.](images/cdmp-formula12.png)

![Muestra la segunda parte del sistema lineal 3?3.](images/cdmp-formula13.gif)![Muestra el valor de t subíndice b al final de la segunda parte del sistema lineal 3?3.](images/cdmp-formula14.gif)

*X <sub>W,</sub>**Y <sub>W,</sub>**Z <sub>W</sub>*

![Muestra la parte final del procedimiento para resolver un sistema lineal 3?3.](images/cdmp-formula15.png)

Una vez determinada la matriz tmulus, la determinación de las curvas de tono sigue el enfoque estándar. En el caso de las pantallas de CRT, se supone que los canales individuales siguen el modelo "GOG":

![Muestra la fórmula para el modelo "G O G".](images/cdmp-formula16.png)

donde *k <sub>g</sub>* es la "ganancia", 1 -*k <sub>g</sub>* es el "desplazamiento" y ? es el "gamma". La matriz inversa de la matriz tmulmulus se aplica a los datos XYZ de los neutros para obtener los datos RGB lineales, que luego se correlacionan con los valores RGB digitales mediante la regresión no lineal en el modelo GOG. Estas características no tienen que ser las mismas para los canales R, G y B y, por lo general, no son las mismas.

Berns 1: Principios de la tecnología de color de \[ \] *Berns, Billmeyer y Saltzman,* 3 <sub>rd</sub> Ed. John Wiley & Sons (2000).

Berns 2: Berns y Blockchain, La función de transferencia digital a radiométrica para pantallas CRT controladas por \[ \] pc, *CIE Expert Symer 97 Standards for Imaging Technology*, noviembre de 1997.

Berns 3: Berns,Ría y Taplin, Estimación de las emisiones de Black-Level de \[ \] Computer-Controlled Displays, Color Research and *Application*, 28: 379-383 Wiley Periodicals, Inc. (2003)

Lugar 1: Azul, Tecnología de color para dispositivos de creación de imágenes \[ \] electrónicas, SPIE (1997) 

Catalina 1: Cargo, Demente y Berns, una propuesta de caracterización precisa del monitor CRT (II) para una extensión al método CIE y su \[ \] comprobación, *Opt. Rev.* 8: 397-408 (2001)

### <a name="lcd-device-model-baseline"></a>Línea de base del modelo de dispositivos USB

La línea base del modelo de dispositivos DE USB es similar a la línea base del modelo de dispositivo CRT. En esta sección se explican las maneras en que el modelado de HOTEL difiere del modelado de CRT.

Una diferencia es que no se puede suponer que las pantallas DE LAC siguen el modelo GOG que se usa para los CRT y que las curvas de tono se obtienen mediante la interpolación de datos medidos. Por eso, el eje neutro del dispositivo se debe muestrear con más frecuencia.

Estos son algunos valores de ejemplo típicos que pueden generar buenos datos para la línea de base del modelo de dispositivos USB:

Rojo: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = 0

Azul: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutros: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.

El proceso de promediación de las colorticidades medidas para obtener las tonticidades de las primarias del dispositivo es más crítico para los LCD que para los CRT. Cuando las medidas XYZ se trazan en el *xy-plane* de la cazticidad, se muestra una situación típica en la figura 1. Observe cómo se desfasa la cromética hacia el punto negro. Esto se debe a que todos los LCD tienen una cierta cantidad de fuga de luz.

![Diagrama que muestra un gráfico de la simplicidad mediante datos sin procesar sin corrección.](images/cdmp-lcd-dmp-figure1.png)

**Figura 1:** Diagrama de siticidad con datos sin procesar sin corrección

Cuando esto se resta de las medidas XYZ sin procesar, se representa una situación típica en la figura 2. Los puntos ahora están agrupados en torno a tres centros, aunque no se encuentran exactamente en ellos. El proceso de promedio descrito para CRT mejora considerablemente los resultados de los LCD.

![Diagrama que muestra un gráfico de la simplicidad mediante datos sin procesar con un punto negro ajustado.](images/cdmp-lcd-dmp-figure2.png)

**Figura 2:** Diagrama de siticidad con datos con punto negro ajustado

### <a name="rgb-capture-device-model-baseline"></a>Línea base del modelo de dispositivo de captura RGB

El modelo de dispositivo de captura RGB de línea base es una subclase de la clase IDeviceModel. En la caracterización colorimétrica de los dispositivos de captura de colores, como escáneres y cámaras digitales, se usa el siguiente enfoque. Un destino que consta de revisiones de color con valores conocidos de CIEXYZ se captura mediante el dispositivo de captura. El resultado de la captura es una imagen de mapa de bits RGB en la que el color de cada revisión se codifica en un valor RGB. Estos valores RGB de dispositivo son específicos de un dispositivo de captura determinado. El objetivo de la caracterización colorimétrica es establecer una relación empírica entre los valores RGB del dispositivo y los valores CIEXYZ, o una transformación matemática de RGB a XYZ que modele con la mayor precisión posible el comportamiento del dispositivo de captura.

Este tipo de transformación matemática se puede modelar razonablemente mediante polinomios de grados bajos. Este procedimiento se detalla en la documentación, por ejemplo, Entre \[ 92 \] y \[ 97. \] En La 97, se notifica un enfoque que usa un conjunto de tres \[ \] polinomios con 3, 6, 8, 9, 11, 14 o 20 términos en las variables R, G y B, mientras que los tres polinómicos retrocede respectivamente en los componentes X, Y y Z del espacio CIEXYZ. Para el polinómico de 20 términos, el formulario es:

![Muestra el polinómico de 20 términos.](images/cdmp-formula20.png)

Hay expresiones similares para Y y Z. La técnica matemática para ajustar los polinómicos se encuentra dentro de "Regresión lineal multivariante" y se describe en cualquier texto elemental en Estadísticas.

Este método de regresión lineal no minimiza la función objetivo "correcta". Por diseño, la regresión lineal encuentra la solución de mínimos cuadrados, lo que implica que los coeficientes obtenidos minimizarán la suma total de cuadrados de errores en el espacio subyacente, o equivalentemente, la suma de cuadrados de las distancias euclidanas. En la práctica, quiere minimizar la suma de cuadrados de ? Es, donde ? E es uno de los estándares aceptados, como CIE94. Minimizar esta función objetivo es un problema de regresión no lineal.

En el nuevo motor, Lab to XYZ es el espacio de color de CIE en el que se revierte y el polinomial cúbica de 20 términos se usa como modelo para el dispositivo de captura, o coeficientes ls, como, bs, de modo que los polinomios siguientes minimizan la suma de cuadrados de ? E <sub>CIE94</sub> s.

![Muestra un conjunto de fórmulas polinómicas.](images/cdmp-formula21.png)

La solución ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) en el espacio numérico real de 60 dimensiones **R** 203 debe ser tal que se minimice el siguiente error total:

![Muestra el error total que se va a minimizar.](images/cdmp-formula22.png)

donde la suma es a través de todos los pares de puntos de datos (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i,</sub>**v <sub>i</sub>* ) en el conjunto de datos muestreados más puntos de control adicionales que se detallarán a continuación. Se trata de un problema de regresión no lineal porque los parámetros *?<sub> i</sub>*, *a <sub>i</sub>*, * <sub>i</sub>* entrar en la función objective de una manera no lineal (no cuadráticamente).

Dado que la función objective ? es una función no lineal (y no quadratic) de los parámetros *?<sub> i</sub>*, *a <sub>i</sub>* e * <sub>i</sub>*, debe recurrir a técnicas iterativas para resolver el problema de optimización. Dado que la forma de la función objective es una suma de cuadrados, se usa una técnica de optimización estándar denominada Levenberg-Marquardt algoritmo. Se considera el método elegido para los problemas de mínimos cuadrados no lineales. En el caso de algoritmos iterativos como Levdiv-Marquardt, debe proporcionar una suposición inicial. Una buena conjetura inicial suele ser fundamental para encontrar el valor mínimo correcto. En este caso, un buen candidato para la suposición inicial es la solución del problema de regresión lineal. En primer lugar, minimice la suma del cuadrado de distancias euclidanas en el espacio laboratorio, mediante la definición de una función objetivo cuadrática:

![Muestra una función de objetivo cuadrática definida.](images/cdmp-formula23.png)

La solución matemática a este problema de "mínimos cuadrados lineales" es conocida. ¿Porque *?<sub> i</sub>* solo aparece en *el modelado L,* *<sub>i</sub>* solo aparece en el modelado de *u* y * <sub>i</sub>* solo aparece en el modelado de *v;* el problema de optimización se puede descomponer en tres subproblemas: uno para *L,* otro para *u* y otro para *v*. Tenga en cuenta *las ecuaciones L.* (Las *ecuaciones u* y *v siguen* exactamente el mismo argumento). El problema de minimizar la suma de cuadrados de errores en *L* se puede indicar como la solución de la siguiente ecuación de matriz en el sentido de mínimos cuadrados:

![Muestra una ecuación de matriz para L.](images/cdmp-formula24.png)

donde *N* es el número total de puntos de datos (puntos muestreados originales más puntos de control creados de la manera que se describe a continuación). Normalmente, *N* es mucho mayor que 20, por lo que la ecuación anterior está demasiado determinada, lo que requiere una solución de mínimos cuadrados. Una solución de formulario cerrado para **?** está disponible:

![Muestra una solución de formulario cerrado.](images/cdmp-formula25.png)

En la práctica, no se usa la evaluación directa mediante la solución de formulario cerrado porque tiene propiedades numéricas deficientes. En su lugar, se aplica algún tipo de algoritmo de factorización de matriz a la matriz de coeficientes que reduce el sistema de ecuaciones a una forma canónica. En la implementación actual, la descomposición de valores singulares (SVD) se aplica a la matriz **R** y, a continuación, se resuelve el sistema descompuesto resultante.

Solución al problema de regresión lineal, que se indica en ![ Muestra la solución al problema de regresión lineal.](images/cdmp-formula26.png) , se usa como punto inicial del algoritmo Levenberg-Marquardt. En este algoritmo, se calcula un paso de prueba que debe acercar el punto a la solución óptima. El paso de prueba satisface un conjunto de ecuaciones lineales que dependen del valor funcional y los valores de los derivados en el punto actual. Por esta razón, los derivados de la función objective ? con respecto a los parámetros *?<sub> i</sub>*, *a <sub>i</sub> <sub>son</sub>* entradas necesarias para el algoritmo Levenberg-Marquardt. Aunque hay 60 parámetros, hay un acceso directo que permite calcular mucho menos. Por la regla de cadena de cálculo,

![Muestra una ecuación que permite un acceso directo mediante la regla de cadena de cálculo.](images/cdmp-formula27.png)

donde *j* = 1, 2, , 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* son el valor CIELAB del punto de ejemplo *ith* y *R <sub>ij</sub>* es la entrada (*i*,*j* ) de la matriz **R** definida anteriormente. Por lo tanto, en lugar de calcular derivados para 60 parámetros, puede calcular derivados para *L*,*a* y *b* mediante diferencias numéricas hacia delante.

También es necesario configurar un criterio de detención para algoritmos iterativos. En la implementación actual, las iteraciones finalizan si el cuadrado medio DECIE94 es menor que 1 o el número de iteraciones realizadas ha superado 10. El número 10 procede de la experiencia práctica de que, si las primeras iteraciones no reducen significativamente el error, otras iteraciones no ayudarían mucho más que mover el punto de una manera oscilante, es decir, es posible que el algoritmo no converjan. Incluso en el caso de que el algoritmo diverja, podemos estar seguros de que DECIE94 no es peor que lo que iniciamos, es decir, con los parámetros obtenidos de la regresión lineal.

Incluso con el método anterior de regresión no lineal, hay varios problemas con el ajuste. Un problema es que los polinomios tienden a sobreshoot o subshoot más allá de los puntos de datos. Se pueden introducir maxima y minima locales artificiales en el proceso de ajuste. Esto se puede contrarreste mediante polinomios de bajo grado, que es la razón por la que no debe usar más de tres grados. Un aspecto más grave de sobreshooting o subshooting es que, aunque un polinómico puede tomar cualquier valor real en teoría, el espacio que intenta modelar normalmente tiene restricciones físicas y prácticas. CIEXYZ debe tener todos los valores X, Y, Z no negativos, que es una restricción física. En la práctica, solo toman valores de la magnitud de cientos, no miles o superiores. De forma similar, CIELAB o CIELUV tiene sus propias restricciones físicas y prácticas. Cuando el espacio RGB se rellena lo suficiente con puntos de ejemplo, el problema de sobreshooting o subshooting no es grave. Sin embargo, los puntos RGB capturados del dispositivo de captura no suelen rellenar el espacio RGB uniformemente. Los puntos pueden llenar solo el 80 % interno del cubo RGB o, lo que es peor, pueden residir en una multiplicación dimensional inferior. Cuando esto sucede, los polinómicos con regresión pueden hacer un trabajo deficiente al extrapolar los valores más allá de los puntos de datos y, a veces, devolver predicciones no realistas. Quiere un modelo que siempre devuelva valores razonablemente realistas. Esto requiere un método que pueda controlar eficazmente el comportamiento límite de los polinómicos de regresión al imponer un costo adicional a los polinomios que se comportan de forma errática cerca del límite del cubo RGB. Una medida adicional para asegurarse de que los polinómicos siempre devuelven valores realistas se aplica recortando la salida a dentro del locus espectral de CIE.

Es en este momento cuando el modelado del analizador y el modelado de la cámara difieren entre sí. Se espera que el modelo de cámara se extrapola a regiones más allá de los puntos muestreados, incluidos los "resaltados especulares", no se requiere la misma extrapolación para el modelo del analizador. Se espera que el destino del analizador cubra una caracterización similar a los materiales impresos que se examinarán. El modelo del analizador sigue siendo necesario para ser sólido en el sentido de que no debe devolver valores no realistas, pero no es necesaria la extrapolación mucho más allá del destino de caracterización. Para garantizar la solidez, el polinómico L anterior se recorta en 100, es decir, el modelo polinómico se ve obligado a no extrapolarse más allá de "Dmin" del destino del analizador.

Se espera que el modelo de cámara se extrapola a los resaltados especulares, por lo que no se quiere recortar en 100. En su lugar, se usa el algoritmo siguiente.

Los puntos de control artificiales se introducen para controlar el comportamiento de los polinomios en regiones con muestreo insuficiente. Al colocar estratégicamente estos puntos de control con los valores adecuados, sirven para "extraer" los polinómicos en la dirección necesaria. En la implementación actual, se usan ocho puntos de control correspondientes a las esquinas del cubo RGB. Si los valores del dispositivo se normalizan en Unity, estos puntos son:

*R* = 0, *G* = 0, *B* = 0

*R* = 0, *G* = 0, *B* = 1

*R* = 0, *G* = 1, *B* = 0

*R* = 0. *G* = 1, *B* = 1

*R* = 1, *G* = 0, *B* = 0

*R* = 1, *G* = 0, *B* = 1

*R* = 1, *G* = 1, *B* = 0

*R* = 1, *G* = 1, *B* = 1

Excepto para el R G B blanco = 1, que está asociado a un valor  =   =  de CIELAB de *L* = 100, *u* v = 0, se usa el siguiente algoritmo de extrapolación para determinar el valor  =  de CIELAB adecuado al que se va a asociar. Por lo general, para un determinado (*R*,*G*,*B* ), se asocia un peso a cada uno de los (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) en el conjunto de datos muestreados. Hay dos objetivos para asignar el peso. En primer lugar, el peso es inversamente proporcional a la distancia entre (*R*,*G*,*B* ) y (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ). En segundo lugar, desea descartar o asignar el peso 0 a los puntos que tienen un matiz diferente al punto dado *(R,**G*,*B* ). Para tener en cuenta el matiz, tenga en cuenta los puntos que se encuentran dentro de un cono cuyo vértice está en (0, 0, 0), cuyo eje coincide con la unión de línea (0, 0, 0) a (*R*,*G*,*B* ) y cuyo ángulo semi vertical ? satisfies cos ? = 0,9. Vea la figura 3 para obtener una ilustración de este cono.

![Diagrama que muestra la forma del barrio.](images/cdmp-lcd-dmp-figure3.png)

**Figura 3:** Filtrado de los puntos de ejemplo por ángulo y distancia. La forma del barrio representado es solo para fines ilustrativos. La forma real depende de la distancia utilizada; es un barrio con forma de rombo si se usa la norma 1.

Dentro de este cono, se realiza un segundo filtrado basado en la distancia RGB, que usa la norma 1, definida por

![Muestra la fórmula para el segundo filtrado dentro del cono.](images/cdmp-formula28.png)

Con el cono actual, la búsqueda inicial es para los puntos que están a una distancia de 0,1 desde (*R*,*G*,*B* ). Si no se encuentra ningún punto dentro de este radio, el radio aumenta en 0,1 y se reinicia la búsqueda. Si la siguiente red redondeada tampoco tiene ningún punto, el radio aumenta en 0,1. Este proceso continúa hasta que el radio supera MaxDist/5, donde MaxDist = 3, en el caso de 1-norm. Si no se encuentra ningún punto, el cono se amplía reduciendo el cos ? en 0,05, es decir, aumentando el ángulo ? y reiniciar todo el proceso con un radio creciente. Este proceso continúa hasta que se encuentra un conjunto de puntos no vacío o cos ? alcanza 0, es decir, el cono se ha abierto para convertirse en un plano. En este momento, la búsqueda se reinicia aumentando el radio, salvo que la búsqueda continúa hasta que el radio alcanza MaxDist. Esto garantiza que, en el peor de los casos, se encontrará un conjunto de puntos no vacío. El algoritmo se resume en el diagrama de flujo de la figura 4.

![Diagrama que muestra el flujo del algoritmo.](images/cdmp-lcd-dmp-figure4.png)

**Figura 4:** Flow para determinar el conjunto S de puntos de muestra utilizados en la extrapolación para un valor RGB de entrada

Suponiendo que el proceso anterior produce un conjunto no vacío *S* de puntos (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) y correspondiente (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), a continuación, para cada punto de este tipo, se asigna un peso *w <sub>i,</sub>* dado por

![Muestra la fórmula para un peso para cada punto.](images/cdmp-formula29.png)

Por último, el extrapolante se define mediante

![Muestra la definición del extrapolante.](images/cdmp-formula30.png)

Las ecuaciones anteriores constituyen una instancia de los "métodos ponderados de distancia inversa", normalmente denominados métodos Shepard. Al ejecutar cada uno de los ocho puntos de eq (6) a través del algoritmo, se obtienen ocho puntos de control, cada uno con R *,**G*,*B* y *L*,*a*,*valores b,* que se incluyen en el grupo con los datos de ejemplo originales.

Para asegurarse de que el modelo siempre genera valores de color válidos y para la integridad y estabilidad del sistema en toda la canalización de procesamiento de color, debe realizar un recorte final a la salida del modelo polinómico. La gama visual de CIE se describe mediante el componente acromático (*Y* o *L* ) y el componente pótic (*xy* o *a'b',* que están relacionados con el espacio XYZ mediante una transformación projective). En la implementación actual, se usa la siticidad *a'b'* porque está directamente relacionada con el espacio CIELUV. Para cualquier *valor de CIELAB,* primero recorte *L* en un valor no negativo:

![Muestra el recorte de L en un valor no negativo.](images/cdmp-formula31.png)

Para permitir la extrapolación de resaltados especulares, *L* no se recorta en 100, el límite superior "convencional" para *L* en el espacio de laboratorio.

A continuación, *si L* = 0, *a* y *b* se recortan de forma que a =*b =* 0. Si *L* ? 0, calculate

![Muestra la fórmula si L=0.](images/cdmp-formula32.png)

Estos son los componentes de un vector del *diagrama a'b'* del punto blanco (*u?'*,*v?'* ) al color en cuestión. Defina el locus espectral de CIE como la forma convexa de todos los puntos (*a'*,*b'* ), parametrizado por la longitud de onda ?:

![Muestra la fórmula para la longitud de onda.](images/cdmp-formula33.png)

donde ![ muestra las funciones para la coincidencia de colores de CIE.](images/cdmp-formula34.png) son las funciones de coincidencia de colores de CIE para el observador de 2 grados. Si el vector se encuentra fuera del locus de CIE, el color se recorta hasta el punto del locus de CIE que es la intersección del locus y la línea definida por el vector. Vea la figura 5. Si se ha producido un recorte, *el valor a* y *b* se reconstruye restando primero *un ?* y *b?'* del recortado *a'* *y b'* y, a continuación, multiplicando por 13 *L*.

![Diagrama que muestra el gráfico del algoritmo de recorte.](images/cdmp-lcd-dmp-figure5.png)

**Figura 5:** Algoritmo de recorte para valores de laboratorio que están fuera de la gama visual de CIE

En la implementación actual, el locus espectral de CIE en el plano *a'b'* se representa mediante una curva lineal por partes con 35 segmentos (correspondiente a una longitud de onda de 360 nm a 700 nm inclusive). Al ordenar los segmentos de línea para que sus ángulos de subterfundo en el punto blanco sean ascendentes, lo que equivale a longitudes de onda descendentes, el segmento de línea que forma una intersección con el rayo formado por el vector anterior se puede encontrar mediante una búsqueda binaria simple.

### <a name="rgb-printer-device-model-baseline"></a>Línea base del modelo de dispositivo de impresora RGB

Una caracterización de dispositivo de una impresora RGB consiste en construir un modelo empírico del dispositivo que predice el color CIELUV independiente del dispositivo para cualquier valor RGB determinado.

Hay dos maneras de construir el modelo empírico. Una manera es usar los datos del dispositivo para una impresora RGB y la otra es usar datos de parámetros analíticos. En la primera, los datos de medida proporcionados por un usuario para un dispositivo de impresora RGB se usan para construir una tabla de búsqueda 3D (LUT). Los datos de medida constan de valores XYZ para las revisiones RGB muestreadas uniformemente. Los tamaños de muestreo típicos son 9 o 17 para cada componente. Cada revisión se mide con un colorimeter o spectrophotometer en el espacio CIEXYZ. A continuación, el valor XYZ de una revisión se convierte en el valor CIELUV, formando un LUT 3D. En el modelo de dispositivo, se aplica el método de interpolación de la galería al LUT 3D con el fin de predecir los datos CIELUV para un determinado dato RGB. (Confer US Patent 4275413 (Patenta de EE. UU.), Us Patent 4511989 (Flizó), Pero \[ 1 \] . Las dos nociones mencionadas han expirado). Los datos de parámetros analíticos pasados en el segundo método son simplemente un LUT que se creó anteriormente. Normalmente, ese LUT se creó con el primer método, aunque se podría construir a mano.

En la administración de colores actual, el mapa de origen se define como el mapa que va del espacio RGB a un espacio de color CIEXYZ independiente del dispositivo. El mapa de destino se define como el mapa que va del espacio de color CIEXYZ independiente del dispositivo al espacio RGB. Es el inverso del mapa de origen.

El modelo empírico se usa directamente en el mapa de origen. Primero asigna datos RGB determinados en datos CIELUV, que se convierten en datos XYZ. En el mapa de destino, los datos CIEXYZ independientes del dispositivo se convierten primero en datos CIELUV. A continuación, el modelo empírico y el método Newton-Raphson clásico se usan para predecir los mejores datos RGB para los datos CIELUV. Los detalles sobre la conversión de datos CieLUV a RGB son los siguientes:

Después de generar un LUT 3D de RGB a CieLUV, el mapa de RGB a LUV se genera mediante interpolación de color azul en RGB. Este mapa se indica mediante las siguientes ecuaciones:

![Muestra las ecuaciones del mapa de R G B a L U V.](images/cdmp-image125.png)

La inversión del mapa consiste en resolver, para cualquier color ![Muestra L U V.](images/cdmp-image127.png) , el siguiente sistema de ecuaciones no lineales:

![Muestra las ecuaciones no lineales para la lolving de cualquier color L U V.](images/cdmp-image129.png)

Una ecuación no lineal que se basa en el método Newton-Raphson clásico se usa en la nueva CTE. Una suposición inicial, o *a priori* ver, es anterior a <sub>-(R</sub> 0, G 0, B 0 ) se obtiene mediante la búsqueda a través de una "matriz de inicialización" que consta de una cuadrícula uniforme de 8x8x8 de pares calculados previamente (RGB,Luv). Se elige la luv correspondiente RGB más cercana a la L \* u \* \* v. Cada punto de la matriz de valores de matriz se corresponde con el centro de una celda para que las iteraciones no comiencen por un punto en la cara de límite del cubo RGB. En otras palabras, el RGB de las iniciales se define mediante: STEP = 1/8 s <sub>ijk</sub> = (STEP/2 + (i-1) STEP, STEP/2+(j-1)STEP, STEP/2+(k-1)STEP) con i,j,k = 1...8 En el primer paso de Newton-Raphson, la siguiente estimación muestra las variables de la siguiente  ![ estimación.](images/cdmp-image133.png) se obtiene mediante la fórmula :

![Muestra la fórmula para la estimación.](images/cdmp-image135.png)

La iteración se detiene cuando el error (distancia en el espacio CIELUV) es menor que un nivel de tolerancia establecido previamente (0,1 en el CTE) o cuando el número de iteraciones ha superado el número máximo permitido de iteraciones (10 en el CTE). Los valores de la tolerancia y el número de iteraciones se determinaron empíricamente para ser efectivos. En versiones futuras, se puede cambiar el valor de tolerancia.

La matriz Denía se calcula con diferencia hacia delante, excepto en un punto de límite (uno o varios de R, G, B es 1) donde se usa la diferencia hacia atrás en su lugar. En lugar de calcular el inverso de la matriz Denía, el sistema lineal se resuelve directamente mediante Gauss-Jordan eliminación con pivote completo.

Al final de las iteraciones, es posible que la convergencia no se alcance porque Newton-Raphson es un algoritmo "local", es decir, solo funciona bien si empieza con una suposición inicial cercana a la solución verdadera. Si, al final de las iteraciones de Newton-Raphson, no se ha logrado la convergencia dentro de la tolerancia a errores predefinida, las iteraciones se reinician con un nuevo conjunto de valores iniciales, definidos como se muestra a continuación.

Por ejemplo, la mejor solución obtenida hasta ahora es (r, g, b). A partir de esta solución, se derivan N a posteriori, donde N = 4. Intuitivamente, la solución se mueve "hacia el centro" en un tamaño de paso que depende de N. Consulte la figura 6.

![Diagrama que muestra las direcciones de la solución.](images/cdmp-image136.png)

**Figura 6:** La dirección de la solución depende del octante en el que se encuentra.

En otras palabras, si r 0,5, el valor del canal R se reduce; de lo &gt; contrario, se aumenta el valor. Hay una lógica similar para los canales G y B. Las definiciones precisas son:

PERTURBATION = 0,5/(N+1)

Dir(r) = -1 si r &gt; 0,5; +1 en caso contrario. De forma similar para Dir(g) y Dir(b)

La jth a posteriori seed, s ????, es (r + Dir(r) \* j \* SETION, g + Dir(g) \* j \* SETION, b + Dir(b) \* j \* SETION)

Pruebe los primeros ???? y si proporciona una nueva solución dentro de la tolerancia a errores, puede detenerse. De lo contrario, pruebe el segundo ???? y así sucesivamente hasta la enésima ????.

Los esquemas de todo el algoritmo se muestran en la figura 7.

![Diagrama que muestra el flujo para invertir el modelo de dispositivo.](images/cdmp-image138.png)

**Figura 7:** Esquemas de invertir el modelo de dispositivo

### <a name="rgb-virtual-device-model-baseline"></a>Línea base del modelo de dispositivo virtual RGB

Este modelo de dispositivo (DM) es un algoritmo simple de reproducción de matriz/tono. La matriz se deriva del punto blanco y las primarias mediante algoritmos de ciencia de colores estándar. La curva de reproducción del tono se deriva de los parámetros de medida según las descripciones DE LA PROPIEDAD de CurveType y ParametricType (o invertidas según sea necesario). Los detalles de los algoritmos internos se proporcionan después de la validación adicional de problemas de alto intervalo dinámico.

El modelo de dispositivo virtual RGB es una curva rgb de reproducción de matriz/tono idealizada similar al diseño de perfil basado en matriz de tres componentes DE LA MATRIX de LA CORTE. Los parámetros de "medición virtual" de la dm incluyen un valor de punto blanco (CIEXYZ absoluto), valores primarios RGB (CIEXYZ absoluto) y una curva de reproducción de tono que se basa en parametricCurveType y CurveType de PARAMETRIC EN FORMATO XML coherente con los esquemas DMP.

La codificación del tipo de función PARAMETRICCurveType y la compatibilidad correspondiente en IRGBVirtualDeviceModelBase se muestran en la tabla siguiente.



| Tipo de función                                         | Parámetros                          | Tipo                                     | Nota:                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Muestra la función 'GammaType'.](images/cdmp-image154.png)<br/> | e<br/>              | GammaType<br/>                 | Implementación común<br/>           |
| ![Muestra la función 'GammaOffsetGainType'.](images/cdmp-image156.png)<br/> | ga b<br/>           | GammaOffsetGainType<br/>       | CIE 122-1966<br/>                    |
| ![Muestra la función 'GammaOffsetGainOffsetType'.](images/cdmp-image158.png)<br/> | ga b c<br/>         | GammaOffsetGainOffsetType<br/> | IEC 61966-3<br/>                     |
| ![Muestra la función 'GammaOffsetGainGainType'.](images/cdmp-image160.png)<br/> | ga b c d<br/>       | GammaOffsetGainGainType<br/>   | IEC 61966-2.1<br/> (sRGB)<br/> |
| ![Muestra una función para los parámetros "g a b c d e f".](images/cdmp-image162.png)<br/> | ga b c d e f<br/>   | N/D<br/>                       | No se admite en WCS<br/>            |



 

La curva de tono de los dispositivos virtuales RGB se aplica en DeviceToColorimetric entre los datos de entrada, pDeviceColors y la multiplicación de la matriz. Para ColorimetricToDevice, se debe usar un método para invertir la curva de tono. En la implementación de línea de base, esto se realiza mediante la interpolación directa en la misma curva de tono que se usa para DeviceToColorimetric.

Las curvas se deben especificar en los perfiles como pares de números en el espacio flotante. El primer número representa los valores de pDeviceColors. El segundo número representa la salida de la curva de tono. Todos los valores de la curva de tono deben estar entre minColorantUsed y maxColorantUsed. Las curvas de tono deben contener al menos dos entradas: una para minColorantUsed y otra para maxColorantUsed. El número máximo de entradas en ToneCurve es 2048. En general, cuando más entradas hay en la tabla, más precisa puede modelar la curva. Se realiza una interpolación lineal por fragmentos entre las entradas.

Puede considerar métodos de interpolación alternativos. Si sabe algo sobre el comportamiento subyacente del dispositivo, puede usar menos muestras y modelar con más precisión con una curva de orden superior. Pero si usa el tipo de curva incorrecto, será muy impreciso. Sin más información, no se puede adivinar el tipo de curva. Por lo tanto, use la interpolación lineal y proporcione muchos puntos de datos.

### <a name="cmyk-printer-device-model-baseline"></a>Línea base del modelo de dispositivo de impresora PRINTER

Una caracterización de dispositivo de una impresora TROP consta de la construcción de un modelo empírico del dispositivo que predice el color impreso para cualquier valor PEM determinado. La caracterización también incluye la inversión de este modelo para que se nos pueda dar una receta del valor VERT para un color determinado que se va a imprimir. Esto se define normalmente en términos de valor CIEXYZ o CIELAB.

Normalmente, se usa un destino IT8.7/3 que contiene revisiones PATCH. Las revisiones constan de muestreo del espacio SPACE de una manera bien definida para que se forme una cuadrícula rectangular (con espaciado no uniforme en C, M, Y y K). A continuación, cada revisión se mide con un colorimeter o spectrophotometer. Las medidas de los valores de CIEXYZ forman después una tabla de búsqueda (LUT), a partir de la cual se construye un modelo empírico de la impresora mediante el método de interpolación de Interpolación. US Patent 4275413 (Patentmoto et al.), US Patent 4511989 (Patentmoto), Hasta \[ 1 \] . Las dos marcas mencionadas han expirado.

Los requisitos específicos para los ejemplos de medida de YER necesarios para que un perfil de modelo de dispositivo se acepte como válido por el modelo de dispositivo de línea base de impresora USB son los siguientes. (El conjunto de ejemplos se describe más claramente como un conjunto de cubos de ejemplo de CMY, cada uno asociado a un nivel K específico).

-   Como mínimo, se deben proporcionar cubos CMY válidos para los niveles K = 0 y K = 100.
-   Los niveles K intermedios pueden estar espaciados de forma no uniforme.
-   Se omitirá cualquier nivel K intermedio sin un cubo CMY válido.
-   Los cubos CMY pueden usar intervalos de muestra no uniformes (espaciado de cuadrícula), pero se debe usar el mismo conjunto de intervalos de muestra en todas las dimensiones C, M e Y del cubo CMY para un nivel K determinado.
-   Cada cubo CMY de nivel K puede usar un número y espaciado diferentes de intervalos de muestra.
-   Todos los cubos de CMY deben contener las "esquinas" del cubo CMY, Es decir, ejemplos de CMY en \[ 0,0,0 \] , \[ 0,0,100 \] , \[ 0,100,0 \] , \[ 100,0,0 \] , \[ 0,100,100, \] \[ 100,0,100 \] , \[ 100,100, 0 \] , \[ 100,100,100 \] .
-   Todos los niveles de cuadrícula de CMY intermedios se deben muestrear por completo en cada canal. En otras palabras, debe existir un ejemplo en cada intersección de cuadrícula 3D dentro del cubo CMY.
-   Para los cubos K = 0 y K = 100 CMY, los cubos 2x2x2 "solo esquinas" son el mínimo aceptado como válido.

    \[NOTA: Para los niveles K=0 y K=100, un cubo CMY de 3x3x3 se procesará como un cubo de "solo esquinas" de 2x2x2; se omite el nivel de muestra intermedio. Los cubos 4x4x4 y más grandes tendrán todos los ejemplos en la cuadrícula usados.\]

-   Para los niveles K intermedios, los cubos CMY de 4x4x4 son el mínimo aceptado como válido.

Un perfil de alta calidad usará cuadrículas de muestreo más finas que el mínimo necesario para la validez, normalmente 9x9x9x9 o superior. Los ejemplos de los destinos IT8.7/3, IT8.7/4 y ECI generan perfiles de modelo de dispositivo (DMP) válidos para el modelo de dispositivo de línea base de impresora SCSI. Aunque este modelo de dispositivo puede omitir las muestras extraneosas (fuera de la cuadrícula) de estos destinos, no se garantiza que pueda hacerlo para otros destinos, por lo que se recomienda que se quiten muestras extraneosas de los conjuntos de medida que van a perfiles para este modelo de dispositivo.

La inversión del modelo de impresora presenta más dificultades. Dado un color de entrada en CIECAM, hay una pregunta sobre si este color está dentro de la gama de impresoras. También hay un problema relacionado con la organización de puntos en el espacio de apariencia de color. Aunque podemos organizar los valores SPACE para que se coloquen en una cuadrícula rectangular, como se hace en el destino IT8.7/3, no se puede decir lo mismo de los colores impresos resultantes, ya que están situados en el espacio de apariencia de color. En general, se dispersan en el espacio de apariencia de color sin ningún patrón concreto.

Por lo general, hay dos enfoques para el problema de inversión de puntos dispersos. Uno de los enfoques es usar una subdivisión geométrica de la gama de impresoras mediante sólidos tridimensionales elementales, como quehedra. Se puede inducer una subdivisión de la gama de impresoras en el espacio de apariencia de color a partir de la subdivisión correspondiente del espacio CMY(K), vea Hung \[ 93 \] , Apartment \[ 97 \] . Este enfoque tiene la ventaja de la simplicidad computacional. En el caso de un hahedron, solo se usan cuatro puntos en una interpolación. Por otro lado, el resultado depende en gran medida de algunos puntos, lo que significa que un error de medición tendrá un efecto significativo en el resultado. El interpolador también tiende a no ser tan suave. El segundo enfoque no supone ninguna subdivisión y se basa en la técnica de interpolación de datos dispersos. Un ejemplo clásico es la técnica de interpolación shepard o método ponderado inverso (vea Shepard \[ \] 68). En este caso, se eligen varios puntos que rodean el punto de entrada de alguna manera, cada uno asignado a un peso, normalmente inversamente proporcional a la distancia, y el interpolador se toma como la media ponderada de los puntos vecinos. En este enfoque, la elección de los puntos vecinos es fundamental para el rendimiento. Aunque demasiados puntos pueden hacer que el interpolante sea inexacto y no suave, demasiados puntos imponen un alto costo computacional, ya que los pesos suelen ser funciones no lineales y costosas de calcular.

Los dos enfoques descritos anteriormente tienen problemas. El enfoque de subdivisión depende fundamentalmente de que los datos sean razonablemente nulos de ruido y, por lo general, el interpolador no es muy suave. La interpolación de datos dispersos es más tolerante al ruido de los datos y, por lo general, proporciona un interpolador más suave, pero es computacionalmente más costoso.

La nueva CTE adopta un enfoque alternativo. El dispositivo NFC se trata como una colección de varios dispositivos CMY, cada uno de los cuales tiene un valor específico de negro (K). Mediante el uso de un algoritmo de selección que toma como parámetros la lumez y el aro, se elige un nivel de negro. Los valores de CMY se obtienen mediante la inversión de la tabla CMY a Luv correspondiente mediante los métodos Newton empleados en otra parte por el algoritmo de impresora RGB.

Siga los pasos que se describen a continuación.

1.  Imprima el destino de caracterización, que es el destino IT8.7/3, o bien un destino que contenga el muestreo del espacio SPACE a intervalos espaciados regular o irregularmente.
2.  Mida el destino mediante un spectrophotometer y convierta las medidas en espacio CIELUV.
3.  Construya el mapa hacia delante de MPER a Luv.
4.  Use el mapa hacia delante para construir un conjunto de asignaciones de CMY a Luv para un intervalo de K valores.
5.  Para cualquier valor luv de entrada, el valor TROP correspondiente se obtiene seleccionando uno de los mapas construidos en el paso 4 anterior e invirtiendo mediante el método de Newton para obtener un conjunto de colores CMY que acompaña al valor K seleccionado.

Los pasos 1 y 2, que son procedimientos estándar, se realizan mediante un programa de generación de perfiles que no forma parte de la nueva CTE. El destino IT8.7/3 contiene un muestreo razonablemente detallado de todos los valores NEO en varios niveles de C, M, Y y K. Como alternativa, se puede usar un destino personalizado con muestreo uniforme de los canales C, M, Y y K. Una vez impreso el destino, se puede usar un spectrophotometer o colorimeter para medir el valor XYZ de cada revisión, y el valor XYZ se puede convertir al valor Luv mediante el modelo CIELUV.

El paso 3, la construcción del mapa hacia delante de SPACE a Luv, se puede lograr mediante la aplicación de cualquier técnica de interpolación conocida, como el método multilineal o el proceso de interpolación, en la cuadrícula rectangular del espacio LICO. En la nueva CTE, se usa una interpolación dimensional 4 dimensional. Dado que las cuadrículas de muestreo de CMY suelen ser diferentes en cada nivel de K, usamos una técnica de super muestreo, como se detalla a continuación. Para un punto SANDWICH determinado, los niveles K de sándwich se determinan primero en función del valor K. A continuación, introduzca una "super cuadrícula" en cada nivel K que sea una unión de las cuadrículas de CMY en cada uno de los dos niveles K. En cada nivel K, el valor luv de cualquier punto de cuadrícula recién introducido se obtiene mediante una interpolación unidimensional de unidimensional dentro de ese nivel K. Por último, en esta nueva cuadrícula se realiza una interpolación unidimensional de 4 dimensiones para el punto MULTIDIMENSIONAL específico.

![Diagrama que muestra el supermuestreo.](images/cdmp-image163.png)

**Figura 8:** Supermuestreo

En el paso 4 se crea un conjunto de tablas de búsqueda (LUT) de CMY a Luv. El mapa hacia delante construido en el paso 3 se llama repetidamente para volver a muestrear el espacio SPACE. El espacio de color SPACE se muestrea con un espaciado uniforme de K y un muestreo de CMY diferente, pero espaciado uniformemente.

El paso 5 es un procedimiento para obtener el valor de BOOLEAN mediante los LUT construidos en el paso 4 para cualquier punto luv de entrada. El valor adecuado de K se elige analizando la lumez, así como el grado de color en el luv solicitado. Una vez seleccionada la tabla, los valores de CMY se obtienen de la tabla mediante el método de Newton (como se documentó anteriormente en el modelo de dispositivo de impresora RGB).

El espacio CIELUV se usa en el modelo de impresora en lugar de en CIEJab porque el modelo de dispositivo debe basarse únicamente en datos colorimétricos disponibles en el DMP. El DMP contiene datos colorimétricos para cada revisión medida, incluido el punto blanco del medio, por lo que es posible convertir datos CIEXYZ en datos CIELUV. Sin embargo, no es posible convertir a CIECAM02 JCh o Jab, porque no hay acceso a la información de la condición de visualización en el DMP.

### <a name="rgb-projector-device-model-baseline"></a>Línea base del modelo de dispositivo del proyector RGB

Nota: Muchos proyectores RGB tienen más de un modo de funcionamiento. En un modo, que suele ser el predeterminado y podría denominarse algo parecido a "presentación", la respuesta de color del proyector está optimizada para obtener el máximo brillo. Sin embargo, en este modo, el proyector pierde la capacidad de reproducir colores claros y ligeramente tótices, como amarillos amarillos y algunos tonos de tonalidad. En otro modo, a menudo denominado "película", "vídeo" o "sRGB", el proyector está optimizado para la reproducción de imágenes realistas y escenas naturales. En este modo, se negocia el brillo máximo para mejorar la calidad general de la reproducción del color. Para obtener una reproducción satisfactoria del color con proyectores RGB, es necesario colocar el proyector en un modo en el que se pueda reproducir una gama suave de colores.

![Diagrama que muestra un modelo de dispositivo D L P.](images/cdmp-image167.png)

**Figura 9:** Modelo de dispositivo DLP

Un valor RGB entrante pasa a través de dos rutas de cálculo. El primero es el modelo de matriz, que da como resultado un valor XYZ. Esto va seguido inmediatamente de la conversión de XYZ a Luv. La segunda es la interpolación de LUT no uniforme mediante interpolación de paréntesis. La salida de la interpolación ya está en el espacio Luv por construcción. Las dos salidas se agregan para obtener el valor de Luv predicho. Por último, se convierte en XYZ, que es la salida esperada del modelo colorimétrico para el dispositivo DLP.

Puesto que los proyectores son dispositivos de visualización, también admiten la inversión del modelo, es decir, la transformación de XYZ a RGB. Dado que el modelo de dispositivo transforma el espacio RGB en espacio XYZ, que son tridimensionales, la inversión equivale a resolver tres ecuaciones no lineales en tres desconocidos. Esto se puede hacer mediante técnicas estándar de resolución de ecuaciones, como Newton-Raphson. Sin embargo, es preferible convertir PRIMERO XYZ en Luv y, a continuación, invertir la transformación Luv To RGB, porque el espacio luv es más perceptualmente lineal que el espacio XYZ.

### <a name="icc-device-model-baseline"></a>Línea de base del modelo de dispositivo DE LAC

La interoperabilidad del flujo de trabajo CITE ICC se habilita mediante la creación de un perfil de modelo de dispositivo de línea de base de dispositivo de dispositivo de línea de base de dispositivo DE CTE que almacena el objeto de perfil y crea una transformación DE LAN mediante un perfil XYZ sin operación. A continuación, esta transformación se usa para traducir entre los colores de dispositivo y CIEXYZ.

![Diagrama que muestra la interoperabilidad del flujo de trabajo de C I T E I C C.](images/cdmp-image168.png)

**Figura 10:** Interoperabilidad del flujo de trabajo DE CITECCI

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de administración de colores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos y esquemas del Sistema de colores de Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





